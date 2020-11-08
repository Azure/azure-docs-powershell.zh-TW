---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-azstorageblobqueryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobQueryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobQueryConfig.md
ms.openlocfilehash: ec1b3b7ab7cd0ddbbdb0b938149f03755563a742
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129740"
---
# <span data-ttu-id="19d9c-101">New-AzStorageBlobQueryConfig</span><span class="sxs-lookup"><span data-stu-id="19d9c-101">New-AzStorageBlobQueryConfig</span></span>

## <span data-ttu-id="19d9c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="19d9c-102">SYNOPSIS</span></span>
<span data-ttu-id="19d9c-103">建立 blob 查詢設定物件，可在 AzStorageBlobQueryResult 中使用。</span><span class="sxs-lookup"><span data-stu-id="19d9c-103">Creates a blob query configuration object, which can be used in Get-AzStorageBlobQueryResult.</span></span>

## <span data-ttu-id="19d9c-104">句法</span><span class="sxs-lookup"><span data-stu-id="19d9c-104">SYNTAX</span></span>

### <span data-ttu-id="19d9c-105">Csv (預設) </span><span class="sxs-lookup"><span data-stu-id="19d9c-105">Csv (Default)</span></span>
```
New-AzStorageBlobQueryConfig [-AsCsv] [-RecordSeparator <String>] [-ColumnSeparator <String>]
 [-QuotationCharacter <Char>] [-EscapeCharacter <Char>] [-HasHeader] [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="19d9c-106">Json</span><span class="sxs-lookup"><span data-stu-id="19d9c-106">Json</span></span>
```
New-AzStorageBlobQueryConfig [-AsJson] [-RecordSeparator <String>] [-AsJob] [<CommonParameters>]
```

## <span data-ttu-id="19d9c-107">說明</span><span class="sxs-lookup"><span data-stu-id="19d9c-107">DESCRIPTION</span></span>
<span data-ttu-id="19d9c-108">**AzStorageBlobQueryConfig** Cmdlet 會建立 blob 查詢設定物件，可在 AzStorageBlobQueryResult 中使用。</span><span class="sxs-lookup"><span data-stu-id="19d9c-108">The **New-AzStorageBlobQueryConfig** cmdlet creates a blob query configuration object, which can be used in Get-AzStorageBlobQueryResult.</span></span>

## <span data-ttu-id="19d9c-109">示例</span><span class="sxs-lookup"><span data-stu-id="19d9c-109">EXAMPLES</span></span>

### <span data-ttu-id="19d9c-110">範例1：建立 blob 查詢設定及查詢 blob</span><span class="sxs-lookup"><span data-stu-id="19d9c-110">Example 1: Create blob query configures , and query a blob</span></span>
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

<span data-ttu-id="19d9c-111">這個命令首先將輸入設定物件建立為 csv，並將 [輸出設定] 物件設為 json，然後使用2個配置來查詢 blob。</span><span class="sxs-lookup"><span data-stu-id="19d9c-111">This command first create input configuration object as csv, and output configuration object as json, then use the 2 configurations to query blob.</span></span>

## <span data-ttu-id="19d9c-112">參數</span><span class="sxs-lookup"><span data-stu-id="19d9c-112">PARAMETERS</span></span>

### <span data-ttu-id="19d9c-113">-AsCsv</span><span class="sxs-lookup"><span data-stu-id="19d9c-113">-AsCsv</span></span>
<span data-ttu-id="19d9c-114">指示建立 CSV 的 Blob 查詢設定。</span><span class="sxs-lookup"><span data-stu-id="19d9c-114">Indicate to create a Blob Query Configuration for CSV.</span></span>

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

### <span data-ttu-id="19d9c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="19d9c-115">-AsJob</span></span>
<span data-ttu-id="19d9c-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="19d9c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="19d9c-117">-AsJson</span><span class="sxs-lookup"><span data-stu-id="19d9c-117">-AsJson</span></span>
<span data-ttu-id="19d9c-118">指示建立 Json 的 Blob 查詢設定。</span><span class="sxs-lookup"><span data-stu-id="19d9c-118">Indicate to create a Blob Query Configuration for Json.</span></span>

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

### <span data-ttu-id="19d9c-119">-ColumnSeparator</span><span class="sxs-lookup"><span data-stu-id="19d9c-119">-ColumnSeparator</span></span>
<span data-ttu-id="19d9c-120">可選.</span><span class="sxs-lookup"><span data-stu-id="19d9c-120">Optional.</span></span>
<span data-ttu-id="19d9c-121">用來分隔欄的字串。</span><span class="sxs-lookup"><span data-stu-id="19d9c-121">The string used to separate columns.</span></span>

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

### <span data-ttu-id="19d9c-122">-EscapeCharacter</span><span class="sxs-lookup"><span data-stu-id="19d9c-122">-EscapeCharacter</span></span>
<span data-ttu-id="19d9c-123">可選.</span><span class="sxs-lookup"><span data-stu-id="19d9c-123">Optional.</span></span>
<span data-ttu-id="19d9c-124">用來做為逸出字元的字元。</span><span class="sxs-lookup"><span data-stu-id="19d9c-124">The char used as an escape character.</span></span>

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

### <span data-ttu-id="19d9c-125">-HasHeader</span><span class="sxs-lookup"><span data-stu-id="19d9c-125">-HasHeader</span></span>
<span data-ttu-id="19d9c-126">可選.</span><span class="sxs-lookup"><span data-stu-id="19d9c-126">Optional.</span></span>
<span data-ttu-id="19d9c-127">表示它代表資料有標題。</span><span class="sxs-lookup"><span data-stu-id="19d9c-127">Indicate it represent the data has headers.</span></span>

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

### <span data-ttu-id="19d9c-128">-QuotationCharacter</span><span class="sxs-lookup"><span data-stu-id="19d9c-128">-QuotationCharacter</span></span>
<span data-ttu-id="19d9c-129">可選.</span><span class="sxs-lookup"><span data-stu-id="19d9c-129">Optional.</span></span>
<span data-ttu-id="19d9c-130">用來為特定欄位加上引號的字元。</span><span class="sxs-lookup"><span data-stu-id="19d9c-130">The char used to quote a specific field.</span></span>

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

### <span data-ttu-id="19d9c-131">-RecordSeparator</span><span class="sxs-lookup"><span data-stu-id="19d9c-131">-RecordSeparator</span></span>
<span data-ttu-id="19d9c-132">可選.</span><span class="sxs-lookup"><span data-stu-id="19d9c-132">Optional.</span></span>
<span data-ttu-id="19d9c-133">用來分隔記錄的字串。</span><span class="sxs-lookup"><span data-stu-id="19d9c-133">The string used to separate records.</span></span>

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

### <span data-ttu-id="19d9c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19d9c-134">CommonParameters</span></span>
<span data-ttu-id="19d9c-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="19d9c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19d9c-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="19d9c-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19d9c-137">輸入</span><span class="sxs-lookup"><span data-stu-id="19d9c-137">INPUTS</span></span>

### <span data-ttu-id="19d9c-138">所有</span><span class="sxs-lookup"><span data-stu-id="19d9c-138">None</span></span>

## <span data-ttu-id="19d9c-139">輸出</span><span class="sxs-lookup"><span data-stu-id="19d9c-139">OUTPUTS</span></span>

### <span data-ttu-id="19d9c-140">PSBlobQueryTextConfiguration WindowsAzure. ResourceModel。</span><span class="sxs-lookup"><span data-stu-id="19d9c-140">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration</span></span>

## <span data-ttu-id="19d9c-141">筆記</span><span class="sxs-lookup"><span data-stu-id="19d9c-141">NOTES</span></span>

## <span data-ttu-id="19d9c-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="19d9c-142">RELATED LINKS</span></span>