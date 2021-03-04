---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 4E9EA2E9-4BE2-4530-BC2B-D369C016CD8C
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/join-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Join-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Join-AzDataLakeStoreItem.md
ms.openlocfilehash: 9a2e0f7abbf9fa6797b4ced7c6e841b51a63a9dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907893"
---
# <span data-ttu-id="86dbd-101">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="86dbd-101">Join-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="86dbd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="86dbd-102">SYNOPSIS</span></span>
<span data-ttu-id="86dbd-103">加入一或多個檔案，在 Data Lake Store 中建立一個檔案。</span><span class="sxs-lookup"><span data-stu-id="86dbd-103">Joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="86dbd-104">語法</span><span class="sxs-lookup"><span data-stu-id="86dbd-104">SYNTAX</span></span>

```
Join-AzDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86dbd-105">描述</span><span class="sxs-lookup"><span data-stu-id="86dbd-105">DESCRIPTION</span></span>
<span data-ttu-id="86dbd-106">**Join-AzDataLakeStoreItem** Cmdlet 會聯集一或多個檔案，在 Data Lake Store 中建立一個檔案。</span><span class="sxs-lookup"><span data-stu-id="86dbd-106">The **Join-AzDataLakeStoreItem** cmdlet joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="86dbd-107">例子</span><span class="sxs-lookup"><span data-stu-id="86dbd-107">EXAMPLES</span></span>

### <span data-ttu-id="86dbd-108">範例 1：聯聯兩個專案</span><span class="sxs-lookup"><span data-stu-id="86dbd-108">Example 1: Join two items</span></span>
```
PS C:\>Join-AzDataLakeStoreItem -AccountName "ContosoADL" -Paths "/MyFiles/File01.txt","/MyFiles/File02.txt" -Destination "/MyFiles/CombinedFile.txt"
```

<span data-ttu-id="86dbd-109">此命令會聯File01.txtFile02.txt，以建立檔案CombinedFile.txt。</span><span class="sxs-lookup"><span data-stu-id="86dbd-109">This command joins File01.txt and File02.txt to create the file CombinedFile.txt.</span></span>

## <span data-ttu-id="86dbd-110">參數</span><span class="sxs-lookup"><span data-stu-id="86dbd-110">PARAMETERS</span></span>

### <span data-ttu-id="86dbd-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="86dbd-111">-Account</span></span>
<span data-ttu-id="86dbd-112">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="86dbd-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="86dbd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86dbd-113">-DefaultProfile</span></span>
<span data-ttu-id="86dbd-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="86dbd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86dbd-115">-目的地</span><span class="sxs-lookup"><span data-stu-id="86dbd-115">-Destination</span></span>
<span data-ttu-id="86dbd-116">指定聯聯專案的 Data Lake Store 路徑，從根目錄開始 (/) 。</span><span class="sxs-lookup"><span data-stu-id="86dbd-116">Specifies the Data Lake Store path for the joined item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="86dbd-117">-強制</span><span class="sxs-lookup"><span data-stu-id="86dbd-117">-Force</span></span>
<span data-ttu-id="86dbd-118">表示此作業可以覆寫目標檔案 ，如果已存在。</span><span class="sxs-lookup"><span data-stu-id="86dbd-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="86dbd-119">-路徑</span><span class="sxs-lookup"><span data-stu-id="86dbd-119">-Paths</span></span>
<span data-ttu-id="86dbd-120">指定要合併之檔案的 Data Lake Store 路徑陣列，從根目錄開始 (/) 。</span><span class="sxs-lookup"><span data-stu-id="86dbd-120">Specifies an array of Data Lake Store paths of the files to combine, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="86dbd-121">-確認</span><span class="sxs-lookup"><span data-stu-id="86dbd-121">-Confirm</span></span>
<span data-ttu-id="86dbd-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="86dbd-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86dbd-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86dbd-123">-WhatIf</span></span>
<span data-ttu-id="86dbd-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="86dbd-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86dbd-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="86dbd-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86dbd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86dbd-126">CommonParameters</span></span>
<span data-ttu-id="86dbd-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="86dbd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86dbd-128">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="86dbd-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86dbd-129">輸入</span><span class="sxs-lookup"><span data-stu-id="86dbd-129">INPUTS</span></span>

### <span data-ttu-id="86dbd-130">System.String</span><span class="sxs-lookup"><span data-stu-id="86dbd-130">System.String</span></span>

### <span data-ttu-id="86dbd-131">Microsoft.Azure.Commands.DataLakeStore.models.DataLakeStorePathInstance[]</span><span class="sxs-lookup"><span data-stu-id="86dbd-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span></span>

### <span data-ttu-id="86dbd-132">Microsoft.Azure.Commands.DataLakeStore.models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="86dbd-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="86dbd-133">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="86dbd-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="86dbd-134">輸出</span><span class="sxs-lookup"><span data-stu-id="86dbd-134">OUTPUTS</span></span>

### <span data-ttu-id="86dbd-135">System.String</span><span class="sxs-lookup"><span data-stu-id="86dbd-135">System.String</span></span>

## <span data-ttu-id="86dbd-136">筆記</span><span class="sxs-lookup"><span data-stu-id="86dbd-136">NOTES</span></span>

## <span data-ttu-id="86dbd-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="86dbd-137">RELATED LINKS</span></span>

[<span data-ttu-id="86dbd-138">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="86dbd-138">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="86dbd-139">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="86dbd-139">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="86dbd-140">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="86dbd-140">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="86dbd-141">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="86dbd-141">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="86dbd-142">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="86dbd-142">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="86dbd-143">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="86dbd-143">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


