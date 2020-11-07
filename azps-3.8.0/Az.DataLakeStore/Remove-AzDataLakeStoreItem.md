---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 164DC871-0F0C-4E71-A37A-2B85CE65C2C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItem.md
ms.openlocfilehash: 5f927bd9ef64cc22eda7669e9b0d60127cf503ac
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93797745"
---
# <span data-ttu-id="a3d85-101">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a3d85-101">Remove-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="a3d85-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a3d85-102">SYNOPSIS</span></span>
<span data-ttu-id="a3d85-103">刪除 Data Lake Store 中的檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="a3d85-103">Deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="a3d85-104">句法</span><span class="sxs-lookup"><span data-stu-id="a3d85-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]> [-Recurse] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3d85-105">說明</span><span class="sxs-lookup"><span data-stu-id="a3d85-105">DESCRIPTION</span></span>
<span data-ttu-id="a3d85-106">**AzDataLakeStoreItem** Cmdlet 會刪除 Data Lake store 中的檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="a3d85-106">The **Remove-AzDataLakeStoreItem** cmdlet deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="a3d85-107">示例</span><span class="sxs-lookup"><span data-stu-id="a3d85-107">EXAMPLES</span></span>

### <span data-ttu-id="a3d85-108">範例1：移除多個專案</span><span class="sxs-lookup"><span data-stu-id="a3d85-108">Example 1: Remove multiple items</span></span>
```
PS C:\>Remove-AzDataLakeStoreItem -AccountName "ContosoADL" -Paths "/File01.txt","/MyFiles/File.csv"
```

<span data-ttu-id="a3d85-109">這個命令會從 Data Lake Store 移除 File01.txt 和 File.csv 的檔案。</span><span class="sxs-lookup"><span data-stu-id="a3d85-109">This command removes the files File01.txt and File.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="a3d85-110">參數</span><span class="sxs-lookup"><span data-stu-id="a3d85-110">PARAMETERS</span></span>

### <span data-ttu-id="a3d85-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="a3d85-111">-Account</span></span>
<span data-ttu-id="a3d85-112">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="a3d85-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="a3d85-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3d85-113">-DefaultProfile</span></span>
<span data-ttu-id="a3d85-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a3d85-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3d85-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a3d85-115">-Force</span></span>
<span data-ttu-id="a3d85-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="a3d85-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a3d85-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a3d85-117">-PassThru</span></span>
<span data-ttu-id="a3d85-118">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="a3d85-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a3d85-119">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="a3d85-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a3d85-120">-路徑</span><span class="sxs-lookup"><span data-stu-id="a3d85-120">-Paths</span></span>
<span data-ttu-id="a3d85-121">指定要移除之檔案的 Data Lake Store 路徑陣列，並從根目錄 (/) 。</span><span class="sxs-lookup"><span data-stu-id="a3d85-121">Specifies an array of Data Lake Store paths of the files to remove, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="a3d85-122">-遞迴</span><span class="sxs-lookup"><span data-stu-id="a3d85-122">-Recurse</span></span>
<span data-ttu-id="a3d85-123">表示此操作會刪除目的檔案夾中的所有專案，包括子資料夾。</span><span class="sxs-lookup"><span data-stu-id="a3d85-123">Indicates that this operation deletes all items in the target folder, including subfolders.</span></span>

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

### <span data-ttu-id="a3d85-124">-確認</span><span class="sxs-lookup"><span data-stu-id="a3d85-124">-Confirm</span></span>
<span data-ttu-id="a3d85-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a3d85-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3d85-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3d85-126">-WhatIf</span></span>
<span data-ttu-id="a3d85-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a3d85-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3d85-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a3d85-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3d85-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3d85-129">CommonParameters</span></span>
<span data-ttu-id="a3d85-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a3d85-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3d85-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a3d85-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3d85-132">輸入</span><span class="sxs-lookup"><span data-stu-id="a3d85-132">INPUTS</span></span>

### <span data-ttu-id="a3d85-133">System.object</span><span class="sxs-lookup"><span data-stu-id="a3d85-133">System.String</span></span>

### <span data-ttu-id="a3d85-134">DataLakeStorePathInstance [] 的 DataLakeStore []</span><span class="sxs-lookup"><span data-stu-id="a3d85-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span></span>

### <span data-ttu-id="a3d85-135">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="a3d85-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a3d85-136">輸出</span><span class="sxs-lookup"><span data-stu-id="a3d85-136">OUTPUTS</span></span>

### <span data-ttu-id="a3d85-137">System.object</span><span class="sxs-lookup"><span data-stu-id="a3d85-137">System.Boolean</span></span>

## <span data-ttu-id="a3d85-138">筆記</span><span class="sxs-lookup"><span data-stu-id="a3d85-138">NOTES</span></span>

## <span data-ttu-id="a3d85-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="a3d85-139">RELATED LINKS</span></span>

[<span data-ttu-id="a3d85-140">AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a3d85-140">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="a3d85-141">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a3d85-141">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="a3d85-142">匯入-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a3d85-142">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="a3d85-143">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a3d85-143">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="a3d85-144">新-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a3d85-144">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="a3d85-145">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a3d85-145">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


