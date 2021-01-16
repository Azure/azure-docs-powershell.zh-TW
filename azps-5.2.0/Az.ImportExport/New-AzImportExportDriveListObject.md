---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/new-AzImportExportDriveListObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
ms.openlocfilehash: 54252b82ecb32d26cf44b3b6f745856b755d60d9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98282724"
---
# <span data-ttu-id="e0264-101">New-AzImportExportDriveListObject</span><span class="sxs-lookup"><span data-stu-id="e0264-101">New-AzImportExportDriveListObject</span></span>

## <span data-ttu-id="e0264-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e0264-102">SYNOPSIS</span></span>
<span data-ttu-id="e0264-103">建立 ImportExport 的 DriverList 物件。</span><span class="sxs-lookup"><span data-stu-id="e0264-103">Create a DriverList Object for ImportExport.</span></span>

## <span data-ttu-id="e0264-104">句法</span><span class="sxs-lookup"><span data-stu-id="e0264-104">SYNTAX</span></span>

```
New-AzImportExportDriveListObject [-BitLockerKey <String>] [-BytesSucceeded <Int64>] [-CopyStatus <String>]
 [-DriveHeaderHash <String>] [-DriveId <String>] [-ErrorLogUri <String>] [-ManifestFile <String>]
 [-ManifestHash <String>] [-ManifestUri <String>] [-PercentComplete <Int32>] [-State <DriveState>]
 [-VerboseLogUri <String>] [<CommonParameters>]
```

## <span data-ttu-id="e0264-105">說明</span><span class="sxs-lookup"><span data-stu-id="e0264-105">DESCRIPTION</span></span>
<span data-ttu-id="e0264-106">建立 ImportExport 的 DriverList 物件。</span><span class="sxs-lookup"><span data-stu-id="e0264-106">Create a DriverList Object for ImportExport.</span></span>

## <span data-ttu-id="e0264-107">示例</span><span class="sxs-lookup"><span data-stu-id="e0264-107">EXAMPLES</span></span>

### <span data-ttu-id="e0264-108">範例1：為 ImportExport 作業建立新的 DriveList</span><span class="sxs-lookup"><span data-stu-id="e0264-108">Example 1: Create a new DriveList for ImportExport job</span></span>
```powershell
PS C:\> New-AzImportExportDriveListObject -DriveId "9CA995BA" -BitLockerKey "238810-662376-448998-450120-652806-203390-606320-483076" -ManifestFile "\\DriveManifest.xml" -ManifestHash "109B21108597EF36D5785F08303F3638"

BitLockerKey                                            BytesSucceeded CopyStatus DriveHeaderHash DriveId  ErrorLogUri ManifestFile        ManifestHash                     ManifestUri PercentComplete State VerboseLogUri  
------------                                            -------------- ---------- --------------- -------  ----------- ------------        ------------                     ----------- --------------- ----- ------- 
238810-662376-448998-450120-652806-203390-606320-483076 0                                         9CA995BA             \\DriveManifest.xml 109B21108597EF36D5785F08303F3638             0
```

<span data-ttu-id="e0264-109">這些 Cmdlet 會為 ImportExport 作業建立新的 DriveList。</span><span class="sxs-lookup"><span data-stu-id="e0264-109">These cmdlets create a new DriveList for ImportExport job.</span></span>

## <span data-ttu-id="e0264-110">參數</span><span class="sxs-lookup"><span data-stu-id="e0264-110">PARAMETERS</span></span>

### <span data-ttu-id="e0264-111">-BitLockerKey</span><span class="sxs-lookup"><span data-stu-id="e0264-111">-BitLockerKey</span></span>
<span data-ttu-id="e0264-112">用來加密磁片磁碟機的 BitLocker 金鑰。</span><span class="sxs-lookup"><span data-stu-id="e0264-112">The BitLocker key used to encrypt the drive.</span></span>

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

### <span data-ttu-id="e0264-113">-BytesSucceeded</span><span class="sxs-lookup"><span data-stu-id="e0264-113">-BytesSucceeded</span></span>
<span data-ttu-id="e0264-114">已成功地傳送磁片磁碟機的位元組數。</span><span class="sxs-lookup"><span data-stu-id="e0264-114">Bytes successfully transferred for the drive.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0264-115">-CopyStatus</span><span class="sxs-lookup"><span data-stu-id="e0264-115">-CopyStatus</span></span>
<span data-ttu-id="e0264-116">資料傳輸處理常式的詳細狀態。</span><span class="sxs-lookup"><span data-stu-id="e0264-116">Detailed status about the data transfer process.</span></span>
<span data-ttu-id="e0264-117">除非磁碟機處於轉移狀態，否則不會在回應中傳回此欄位。</span><span class="sxs-lookup"><span data-stu-id="e0264-117">This field is not returned in the response until the drive is in the Transferring state.</span></span>

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

### <span data-ttu-id="e0264-118">-DriveHeaderHash</span><span class="sxs-lookup"><span data-stu-id="e0264-118">-DriveHeaderHash</span></span>
<span data-ttu-id="e0264-119">磁片磁碟機標頭雜湊值。</span><span class="sxs-lookup"><span data-stu-id="e0264-119">The drive header hash value.</span></span>

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

### <span data-ttu-id="e0264-120">-DriveId</span><span class="sxs-lookup"><span data-stu-id="e0264-120">-DriveId</span></span>
<span data-ttu-id="e0264-121">磁碟機的硬體序列值（不含空格）。</span><span class="sxs-lookup"><span data-stu-id="e0264-121">The drive's hardware serial number, without spaces.</span></span>

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

### <span data-ttu-id="e0264-122">-ErrorLogUri</span><span class="sxs-lookup"><span data-stu-id="e0264-122">-ErrorLogUri</span></span>
<span data-ttu-id="e0264-123">指向內含資料傳送操作之錯誤記錄的 blob 的 URI。</span><span class="sxs-lookup"><span data-stu-id="e0264-123">A URI that points to the blob containing the error log for the data transfer operation.</span></span>

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

### <span data-ttu-id="e0264-124">-ManifestFile</span><span class="sxs-lookup"><span data-stu-id="e0264-124">-ManifestFile</span></span>
<span data-ttu-id="e0264-125">磁碟機上資訊清單檔案的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="e0264-125">The relative path of the manifest file on the drive.</span></span>

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

### <span data-ttu-id="e0264-126">-ManifestHash</span><span class="sxs-lookup"><span data-stu-id="e0264-126">-ManifestHash</span></span>
<span data-ttu-id="e0264-127">磁片磁碟機上的資訊清單檔案的 Base16 編碼 MD5 雜湊值。</span><span class="sxs-lookup"><span data-stu-id="e0264-127">The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>

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

### <span data-ttu-id="e0264-128">-ManifestUri</span><span class="sxs-lookup"><span data-stu-id="e0264-128">-ManifestUri</span></span>
<span data-ttu-id="e0264-129">指向內含磁片磁碟機資訊清單檔案之 blob 的 URI。</span><span class="sxs-lookup"><span data-stu-id="e0264-129">A URI that points to the blob containing the drive manifest file.</span></span>

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

### <span data-ttu-id="e0264-130">-百分比</span><span class="sxs-lookup"><span data-stu-id="e0264-130">-PercentComplete</span></span>
<span data-ttu-id="e0264-131">已完成磁片磁碟機的百分比。</span><span class="sxs-lookup"><span data-stu-id="e0264-131">Percentage completed for the drive.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0264-132">-State</span><span class="sxs-lookup"><span data-stu-id="e0264-132">-State</span></span>
<span data-ttu-id="e0264-133">磁片磁碟機的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="e0264-133">The drive's current state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Support.DriveState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0264-134">-VerboseLogUri</span><span class="sxs-lookup"><span data-stu-id="e0264-134">-VerboseLogUri</span></span>
<span data-ttu-id="e0264-135">指向內含資料傳輸作業詳細資料記錄之 blob 的 URI。</span><span class="sxs-lookup"><span data-stu-id="e0264-135">A URI that points to the blob containing the verbose log for the data transfer operation.</span></span>

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

### <span data-ttu-id="e0264-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0264-136">CommonParameters</span></span>
<span data-ttu-id="e0264-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e0264-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0264-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e0264-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0264-139">輸入</span><span class="sxs-lookup"><span data-stu-id="e0264-139">INPUTS</span></span>

## <span data-ttu-id="e0264-140">輸出</span><span class="sxs-lookup"><span data-stu-id="e0264-140">OUTPUTS</span></span>

### <span data-ttu-id="e0264-141">IDriveStatus （ImportExport）。 Api20161101。</span><span class="sxs-lookup"><span data-stu-id="e0264-141">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus</span></span>

## <span data-ttu-id="e0264-142">筆記</span><span class="sxs-lookup"><span data-stu-id="e0264-142">NOTES</span></span>

<span data-ttu-id="e0264-143">別名</span><span class="sxs-lookup"><span data-stu-id="e0264-143">ALIASES</span></span>

## <span data-ttu-id="e0264-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="e0264-144">RELATED LINKS</span></span>

