---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 4E9EA2E9-4BE2-4530-BC2B-D369C016CD8C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Join-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Join-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 1f09d1da5ab4ad88ff16be56affaa582ad1e24d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452512"
---
# <span data-ttu-id="425d0-101">Join-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="425d0-101">Join-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="425d0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="425d0-102">SYNOPSIS</span></span>
<span data-ttu-id="425d0-103">加入一或多個檔案，在 Data Lake Store 中建立一個檔案。</span><span class="sxs-lookup"><span data-stu-id="425d0-103">Joins one or more files to create one file in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="425d0-104">句法</span><span class="sxs-lookup"><span data-stu-id="425d0-104">SYNTAX</span></span>

```
Join-AzureRmDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="425d0-105">說明</span><span class="sxs-lookup"><span data-stu-id="425d0-105">DESCRIPTION</span></span>
<span data-ttu-id="425d0-106">**AzureRmDataLakeStoreItem** Cmdlet 加入一或多個檔案，以便在 Data Lake store 中建立一個檔案。</span><span class="sxs-lookup"><span data-stu-id="425d0-106">The **Join-AzureRmDataLakeStoreItem** cmdlet joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="425d0-107">示例</span><span class="sxs-lookup"><span data-stu-id="425d0-107">EXAMPLES</span></span>

### <span data-ttu-id="425d0-108">範例1：加入兩個專案</span><span class="sxs-lookup"><span data-stu-id="425d0-108">Example 1: Join two items</span></span>
```
PS C:\>Join-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Paths "/MyFiles/File01.txt","/MyFiles/File02.txt" -Destination "/MyFiles/CombinedFile.txt"
```

<span data-ttu-id="425d0-109">這個命令會加入 File01.txt 並 File02.txt，以建立 CombinedFile.txt 的檔案。</span><span class="sxs-lookup"><span data-stu-id="425d0-109">This command joins File01.txt and File02.txt to create the file CombinedFile.txt.</span></span>

## <span data-ttu-id="425d0-110">參數</span><span class="sxs-lookup"><span data-stu-id="425d0-110">PARAMETERS</span></span>

### <span data-ttu-id="425d0-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="425d0-111">-Account</span></span>
<span data-ttu-id="425d0-112">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="425d0-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="425d0-113">-目的地</span><span class="sxs-lookup"><span data-stu-id="425d0-113">-Destination</span></span>
<span data-ttu-id="425d0-114">指定已加入專案的資料 Lake Store 路徑，從根目錄 (/) 開始。</span><span class="sxs-lookup"><span data-stu-id="425d0-114">Specifies the Data Lake Store path for the joined item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="425d0-115">-Force</span><span class="sxs-lookup"><span data-stu-id="425d0-115">-Force</span></span>
<span data-ttu-id="425d0-116">表示此操作可以覆寫目標檔案（如果該檔案已經存在的話）。</span><span class="sxs-lookup"><span data-stu-id="425d0-116">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="425d0-117">-路徑</span><span class="sxs-lookup"><span data-stu-id="425d0-117">-Paths</span></span>
<span data-ttu-id="425d0-118">指定要合併之檔案的資料 Lake Store 路徑陣列，並從根目錄 (/) 。</span><span class="sxs-lookup"><span data-stu-id="425d0-118">Specifies an array of Data Lake Store paths of the files to combine, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases: Path

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="425d0-119">-確認</span><span class="sxs-lookup"><span data-stu-id="425d0-119">-Confirm</span></span>
<span data-ttu-id="425d0-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="425d0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="425d0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="425d0-121">-WhatIf</span></span>
<span data-ttu-id="425d0-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="425d0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="425d0-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="425d0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="425d0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="425d0-124">-DefaultProfile</span></span>
<span data-ttu-id="425d0-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="425d0-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="425d0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="425d0-126">CommonParameters</span></span>
<span data-ttu-id="425d0-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="425d0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="425d0-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="425d0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="425d0-129">輸入</span><span class="sxs-lookup"><span data-stu-id="425d0-129">INPUTS</span></span>

## <span data-ttu-id="425d0-130">輸出</span><span class="sxs-lookup"><span data-stu-id="425d0-130">OUTPUTS</span></span>

### <span data-ttu-id="425d0-131">字串</span><span class="sxs-lookup"><span data-stu-id="425d0-131">string</span></span>
<span data-ttu-id="425d0-132">從已加入檔案到所產生之檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="425d0-132">The full path to the resulting file from the joined files.</span></span>

## <span data-ttu-id="425d0-133">筆記</span><span class="sxs-lookup"><span data-stu-id="425d0-133">NOTES</span></span>

## <span data-ttu-id="425d0-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="425d0-134">RELATED LINKS</span></span>

[<span data-ttu-id="425d0-135">AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="425d0-135">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="425d0-136">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="425d0-136">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="425d0-137">匯入-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="425d0-137">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="425d0-138">新-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="425d0-138">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="425d0-139">移除-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="425d0-139">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="425d0-140">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="425d0-140">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


