---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/Az.storage/new-azstorageblobqueryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobQueryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobQueryConfig.md
ms.openlocfilehash: 942bd2635c79a925779239e9746cef53195b202e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915105"
---
# <span data-ttu-id="dfc3f-101">New-AzStorageBlobQueryConfig</span><span class="sxs-lookup"><span data-stu-id="dfc3f-101">New-AzStorageBlobQueryConfig</span></span>

## <span data-ttu-id="dfc3f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="dfc3f-102">SYNOPSIS</span></span>
<span data-ttu-id="dfc3f-103">建立 Blob 查詢設定檔物件，可用於 Get-AzStorageBlobQueryResult。</span><span class="sxs-lookup"><span data-stu-id="dfc3f-103">Creates a blob query configuration object, which can be used in Get-AzStorageBlobQueryResult.</span></span>

## <span data-ttu-id="dfc3f-104">語法</span><span class="sxs-lookup"><span data-stu-id="dfc3f-104">SYNTAX</span></span>

### <span data-ttu-id="dfc3f-105">Csv (預設) </span><span class="sxs-lookup"><span data-stu-id="dfc3f-105">Csv (Default)</span></span>
```
New-AzStorageBlobQueryConfig [-AsCsv] [-RecordSeparator <String>] [-ColumnSeparator <String>]
 [-QuotationCharacter <Char>] [-EscapeCharacter <Char>] [-HasHeader] [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="dfc3f-106">Json</span><span class="sxs-lookup"><span data-stu-id="dfc3f-106">Json</span></span>
```
New-AzStorageBlobQueryConfig [-AsJson] [-RecordSeparator <String>] [-AsJob] [<CommonParameters>]
```

## <span data-ttu-id="dfc3f-107">描述</span><span class="sxs-lookup"><span data-stu-id="dfc3f-107">DESCRIPTION</span></span>
<span data-ttu-id="dfc3f-108">**New-AzStorageBlobQueryConfig** Cmdlet 會建立 Blob 查詢設定檔物件，可用於 Get-AzStorageBlobQueryResult。</span><span class="sxs-lookup"><span data-stu-id="dfc3f-108">The **New-AzStorageBlobQueryConfig** cmdlet creates a blob query configuration object, which can be used in Get-AzStorageBlobQueryResult.</span></span>

## <span data-ttu-id="dfc3f-109">例子</span><span class="sxs-lookup"><span data-stu-id="dfc3f-109">EXAMPLES</span></span>

### <span data-ttu-id="dfc3f-110">範例 1：建立 Blob 查詢設定，以及查詢 Blob</span><span class="sxs-lookup"><span data-stu-id="dfc3f-110">Example 1: Create blob query configures , and query a blob</span></span>
```powershell
PS C:\> $inputconfig = New-AzStorageBlobQueryConfig -AsCsv -ColumnSeparator "," -QuotationCharacter """" -EscapeCharacter "\" -RecordSeparator "`n" -HasHeader

PS C:\> $outputconfig = New-AzStorageBlobQueryConfig -AsJson -RecordSeparator "`n" 

PS C:\> $queryString = "SELECT * FROM BlobStorage WHERE Name = 'a'"

PS C:\> $result = Get-AzStorageBlobQueryResult -Container $containerName -Blob $blobName -QueryString $queryString -ResultFile "c:\resultfile.json" -InputTextConfiguration $inputconfig -OutputTextConfiguration $outputconfig -Context $ctx

PS C:\> $result

BytesScanned FailureCount BlobQueryError
------------ ------------ --------------
         449            0
```

<span data-ttu-id="dfc3f-111">此命令會先將輸入組組物件建立為 csv，再將輸出組組物件建立為 json，然後使用 2 組設定檔查詢 Blob。</span><span class="sxs-lookup"><span data-stu-id="dfc3f-111">This command first create input configuration object as csv, and output configuration object as json, then use the 2 configurations to query blob.</span></span>

## <span data-ttu-id="dfc3f-112">參數</span><span class="sxs-lookup"><span data-stu-id="dfc3f-112">PARAMETERS</span></span>

### <span data-ttu-id="dfc3f-113">-AsCsv</span><span class="sxs-lookup"><span data-stu-id="dfc3f-113">-AsCsv</span></span>
<span data-ttu-id="dfc3f-114">表示要建立 CSV 的 Blob 查詢組塊。</span><span class="sxs-lookup"><span data-stu-id="dfc3f-114">Indicate to create a Blob Query Configuration for CSV.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Csv
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfc3f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dfc3f-115">-AsJob</span></span>
<span data-ttu-id="dfc3f-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="dfc3f-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfc3f-117">-AsJson</span><span class="sxs-lookup"><span data-stu-id="dfc3f-117">-AsJson</span></span>
<span data-ttu-id="dfc3f-118">表示要為 Json 建立 Blob 查詢組塊。</span><span class="sxs-lookup"><span data-stu-id="dfc3f-118">Indicate to create a Blob Query Configuration for Json.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Json
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfc3f-119">-ColumnSeparator</span><span class="sxs-lookup"><span data-stu-id="dfc3f-119">-ColumnSeparator</span></span>
<span data-ttu-id="dfc3f-120">選。</span><span class="sxs-lookup"><span data-stu-id="dfc3f-120">Optional.</span></span>
<span data-ttu-id="dfc3f-121">用來分隔欄的字串。</span><span class="sxs-lookup"><span data-stu-id="dfc3f-121">The string used to separate columns.</span></span>

```yaml
Type: System.String
Parameter Sets: Csv
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfc3f-122">-EscapeCharacter</span><span class="sxs-lookup"><span data-stu-id="dfc3f-122">-EscapeCharacter</span></span>
<span data-ttu-id="dfc3f-123">選。</span><span class="sxs-lookup"><span data-stu-id="dfc3f-123">Optional.</span></span>
<span data-ttu-id="dfc3f-124">用來做為逸出字元的 char。</span><span class="sxs-lookup"><span data-stu-id="dfc3f-124">The char used as an escape character.</span></span>

```yaml
Type: System.Nullable`1[System.Char]
Parameter Sets: Csv
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfc3f-125">-HasHeader</span><span class="sxs-lookup"><span data-stu-id="dfc3f-125">-HasHeader</span></span>
<span data-ttu-id="dfc3f-126">選。</span><span class="sxs-lookup"><span data-stu-id="dfc3f-126">Optional.</span></span>
<span data-ttu-id="dfc3f-127">表示資料有標題。</span><span class="sxs-lookup"><span data-stu-id="dfc3f-127">Indicate it represent the data has headers.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Csv
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfc3f-128">-引號</span><span class="sxs-lookup"><span data-stu-id="dfc3f-128">-QuotationCharacter</span></span>
<span data-ttu-id="dfc3f-129">選。</span><span class="sxs-lookup"><span data-stu-id="dfc3f-129">Optional.</span></span>
<span data-ttu-id="dfc3f-130">用來引用特定欄位的 char。</span><span class="sxs-lookup"><span data-stu-id="dfc3f-130">The char used to quote a specific field.</span></span>

```yaml
Type: System.Char
Parameter Sets: Csv
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfc3f-131">-RecordSeparator</span><span class="sxs-lookup"><span data-stu-id="dfc3f-131">-RecordSeparator</span></span>
<span data-ttu-id="dfc3f-132">選。</span><span class="sxs-lookup"><span data-stu-id="dfc3f-132">Optional.</span></span>
<span data-ttu-id="dfc3f-133">用來分隔記錄的字串。</span><span class="sxs-lookup"><span data-stu-id="dfc3f-133">The string used to separate records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfc3f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfc3f-134">CommonParameters</span></span>
<span data-ttu-id="dfc3f-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="dfc3f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfc3f-136">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="dfc3f-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfc3f-137">輸入</span><span class="sxs-lookup"><span data-stu-id="dfc3f-137">INPUTS</span></span>

### <span data-ttu-id="dfc3f-138">沒有</span><span class="sxs-lookup"><span data-stu-id="dfc3f-138">None</span></span>

## <span data-ttu-id="dfc3f-139">輸出</span><span class="sxs-lookup"><span data-stu-id="dfc3f-139">OUTPUTS</span></span>

### <span data-ttu-id="dfc3f-140">Microsoft.WindowsAzure.Commands.Common.storage.ResourceModel.PSBlobQueryTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="dfc3f-140">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration</span></span>

## <span data-ttu-id="dfc3f-141">筆記</span><span class="sxs-lookup"><span data-stu-id="dfc3f-141">NOTES</span></span>

## <span data-ttu-id="dfc3f-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="dfc3f-142">RELATED LINKS</span></span>
