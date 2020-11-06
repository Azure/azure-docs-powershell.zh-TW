---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 164DC871-0F0C-4E71-A37A-2B85CE65C2C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 40477ad0635f1b832e7d95e459b27102dc68f8db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444560"
---
# <span data-ttu-id="a7e7f-101">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a7e7f-101">Remove-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="a7e7f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a7e7f-102">SYNOPSIS</span></span>
<span data-ttu-id="a7e7f-103">刪除 Data Lake Store 中的檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="a7e7f-103">Deletes a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7e7f-104">句法</span><span class="sxs-lookup"><span data-stu-id="a7e7f-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]> [-Recurse] [-Clean]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7e7f-105">說明</span><span class="sxs-lookup"><span data-stu-id="a7e7f-105">DESCRIPTION</span></span>
<span data-ttu-id="a7e7f-106">**AzureRmDataLakeStoreItem** Cmdlet 會刪除 Data Lake store 中的檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="a7e7f-106">The **Remove-AzureRmDataLakeStoreItem** cmdlet deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="a7e7f-107">示例</span><span class="sxs-lookup"><span data-stu-id="a7e7f-107">EXAMPLES</span></span>

### <span data-ttu-id="a7e7f-108">範例1：移除多個專案</span><span class="sxs-lookup"><span data-stu-id="a7e7f-108">Example 1: Remove multiple items</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Paths "/File01.txt","/MyFiles/File.csv"
```

<span data-ttu-id="a7e7f-109">這個命令會從 Data Lake Store 移除 File01.txt 和 File.csv 的檔案。</span><span class="sxs-lookup"><span data-stu-id="a7e7f-109">This command removes the files File01.txt and File.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="a7e7f-110">參數</span><span class="sxs-lookup"><span data-stu-id="a7e7f-110">PARAMETERS</span></span>

### <span data-ttu-id="a7e7f-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="a7e7f-111">-Account</span></span>
<span data-ttu-id="a7e7f-112">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="a7e7f-112">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7e7f-113">-Clean</span><span class="sxs-lookup"><span data-stu-id="a7e7f-113">-Clean</span></span>
<span data-ttu-id="a7e7f-114">表示使用者想要移除資料夾的所有內容，但不移除資料夾本身</span><span class="sxs-lookup"><span data-stu-id="a7e7f-114">Indicates the user wants to remove all of the contents of the folder, but not the folder itself</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7e7f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7e7f-115">-DefaultProfile</span></span>
<span data-ttu-id="a7e7f-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a7e7f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7e7f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a7e7f-117">-Force</span></span>
<span data-ttu-id="a7e7f-118">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="a7e7f-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7e7f-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a7e7f-119">-PassThru</span></span>
<span data-ttu-id="a7e7f-120">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="a7e7f-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a7e7f-121">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="a7e7f-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7e7f-122">-路徑</span><span class="sxs-lookup"><span data-stu-id="a7e7f-122">-Paths</span></span>
<span data-ttu-id="a7e7f-123">指定要移除之檔案的 Data Lake Store 路徑陣列，並從根目錄 (/) 。</span><span class="sxs-lookup"><span data-stu-id="a7e7f-123">Specifies an array of Data Lake Store paths of the files to remove, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7e7f-124">-遞迴</span><span class="sxs-lookup"><span data-stu-id="a7e7f-124">-Recurse</span></span>
<span data-ttu-id="a7e7f-125">表示此操作會刪除目的檔案夾中的所有專案，包括子資料夾。</span><span class="sxs-lookup"><span data-stu-id="a7e7f-125">Indicates that this operation deletes all items in the target folder, including subfolders.</span></span>
<span data-ttu-id="a7e7f-126">除非您指定 *Clean* 參數，否則目的檔案夾也會被刪除。</span><span class="sxs-lookup"><span data-stu-id="a7e7f-126">Unless you specify the *Clean* parameter, the target folder is also deleted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7e7f-127">-確認</span><span class="sxs-lookup"><span data-stu-id="a7e7f-127">-Confirm</span></span>
<span data-ttu-id="a7e7f-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a7e7f-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7e7f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7e7f-129">-WhatIf</span></span>
<span data-ttu-id="a7e7f-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a7e7f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7e7f-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a7e7f-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7e7f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7e7f-132">CommonParameters</span></span>
<span data-ttu-id="a7e7f-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a7e7f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7e7f-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a7e7f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7e7f-135">輸入</span><span class="sxs-lookup"><span data-stu-id="a7e7f-135">INPUTS</span></span>

### <span data-ttu-id="a7e7f-136">所有</span><span class="sxs-lookup"><span data-stu-id="a7e7f-136">None</span></span>
<span data-ttu-id="a7e7f-137">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="a7e7f-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a7e7f-138">輸出</span><span class="sxs-lookup"><span data-stu-id="a7e7f-138">OUTPUTS</span></span>

### <span data-ttu-id="a7e7f-139">bool</span><span class="sxs-lookup"><span data-stu-id="a7e7f-139">bool</span></span>
<span data-ttu-id="a7e7f-140">如果已指定 PassThru，則會傳回運算的結果。</span><span class="sxs-lookup"><span data-stu-id="a7e7f-140">If PassThru is specified, returns the result of the operation.</span></span>

## <span data-ttu-id="a7e7f-141">筆記</span><span class="sxs-lookup"><span data-stu-id="a7e7f-141">NOTES</span></span>

## <span data-ttu-id="a7e7f-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="a7e7f-142">RELATED LINKS</span></span>

[<span data-ttu-id="a7e7f-143">AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a7e7f-143">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="a7e7f-144">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a7e7f-144">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="a7e7f-145">匯入-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a7e7f-145">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="a7e7f-146">Join-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a7e7f-146">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="a7e7f-147">新-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a7e7f-147">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="a7e7f-148">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a7e7f-148">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


