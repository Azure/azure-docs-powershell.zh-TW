---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/new-AzImportExportDriveListObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
ms.openlocfilehash: 54252b82ecb32d26cf44b3b6f745856b755d60d9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449265"
---
# <span data-ttu-id="50a2a-101">New-AzImportExportDriveListObject</span><span class="sxs-lookup"><span data-stu-id="50a2a-101">New-AzImportExportDriveListObject</span></span>

## <span data-ttu-id="50a2a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="50a2a-102">SYNOPSIS</span></span>
<span data-ttu-id="50a2a-103">建立 ImportExport 的 DriverList 物件。</span><span class="sxs-lookup"><span data-stu-id="50a2a-103">Create a DriverList Object for ImportExport.</span></span>

## <span data-ttu-id="50a2a-104">句法</span><span class="sxs-lookup"><span data-stu-id="50a2a-104">SYNTAX</span></span>

```
New-AzImportExportDriveListObject [-BitLockerKey <String>] [-BytesSucceeded <Int64>] [-CopyStatus <String>]
 [-DriveHeaderHash <String>] [-DriveId <String>] [-ErrorLogUri <String>] [-ManifestFile <String>]
 [-ManifestHash <String>] [-ManifestUri <String>] [-PercentComplete <Int32>] [-State <DriveState>]
 [-VerboseLogUri <String>] [<CommonParameters>]
```

## <span data-ttu-id="50a2a-105">說明</span><span class="sxs-lookup"><span data-stu-id="50a2a-105">DESCRIPTION</span></span>
<span data-ttu-id="50a2a-106">建立 ImportExport 的 DriverList 物件。</span><span class="sxs-lookup"><span data-stu-id="50a2a-106">Create a DriverList Object for ImportExport.</span></span>

## <span data-ttu-id="50a2a-107">示例</span><span class="sxs-lookup"><span data-stu-id="50a2a-107">EXAMPLES</span></span>

### <span data-ttu-id="50a2a-108">範例1：為 ImportExport 作業建立新的 DriveList</span><span class="sxs-lookup"><span data-stu-id="50a2a-108">Example 1: Create a new DriveList for ImportExport job</span></span>
```powershell
PS C:\> New-AzImportExportDriveListObject -DriveId "9CA995BA" -BitLockerKey "238810-662376-448998-450120-652806-203390-606320-483076" -ManifestFile "\\DriveManifest.xml" -ManifestHash "109B21108597EF36D5785F08303F3638"

BitLockerKey                                            BytesSucceeded CopyStatus DriveHeaderHash DriveId  ErrorLogUri ManifestFile        ManifestHash                     ManifestUri PercentComplete State VerboseLogUri  
------------                                            -------------- ---------- --------------- -------  ----------- ------------        ------------                     ----------- --------------- ----- ------- 
238810-662376-448998-450120-652806-203390-606320-483076 0                                         9CA995BA             \\DriveManifest.xml 109B21108597EF36D5785F08303F3638             0
```

<span data-ttu-id="50a2a-109">這些 Cmdlet 會為 ImportExport 作業建立新的 DriveList。</span><span class="sxs-lookup"><span data-stu-id="50a2a-109">These cmdlets create a new DriveList for ImportExport job.</span></span>

## <span data-ttu-id="50a2a-110">參數</span><span class="sxs-lookup"><span data-stu-id="50a2a-110">PARAMETERS</span></span>

### <span data-ttu-id="50a2a-111">-BitLockerKey</span><span class="sxs-lookup"><span data-stu-id="50a2a-111">-BitLockerKey</span></span>
<span data-ttu-id="50a2a-112">用來加密磁片磁碟機的 BitLocker 金鑰。</span><span class="sxs-lookup"><span data-stu-id="50a2a-112">The BitLocker key used to encrypt the drive.</span></span>

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

### <span data-ttu-id="50a2a-113">-BytesSucceeded</span><span class="sxs-lookup"><span data-stu-id="50a2a-113">-BytesSucceeded</span></span>
<span data-ttu-id="50a2a-114">已成功地傳送磁片磁碟機的位元組數。</span><span class="sxs-lookup"><span data-stu-id="50a2a-114">Bytes successfully transferred for the drive.</span></span>

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

### <span data-ttu-id="50a2a-115">-CopyStatus</span><span class="sxs-lookup"><span data-stu-id="50a2a-115">-CopyStatus</span></span>
<span data-ttu-id="50a2a-116">資料傳輸處理常式的詳細狀態。</span><span class="sxs-lookup"><span data-stu-id="50a2a-116">Detailed status about the data transfer process.</span></span>
<span data-ttu-id="50a2a-117">除非磁碟機處於轉移狀態，否則不會在回應中傳回此欄位。</span><span class="sxs-lookup"><span data-stu-id="50a2a-117">This field is not returned in the response until the drive is in the Transferring state.</span></span>

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

### <span data-ttu-id="50a2a-118">-DriveHeaderHash</span><span class="sxs-lookup"><span data-stu-id="50a2a-118">-DriveHeaderHash</span></span>
<span data-ttu-id="50a2a-119">磁片磁碟機標頭雜湊值。</span><span class="sxs-lookup"><span data-stu-id="50a2a-119">The drive header hash value.</span></span>

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

### <span data-ttu-id="50a2a-120">-DriveId</span><span class="sxs-lookup"><span data-stu-id="50a2a-120">-DriveId</span></span>
<span data-ttu-id="50a2a-121">磁碟機的硬體序列值（不含空格）。</span><span class="sxs-lookup"><span data-stu-id="50a2a-121">The drive's hardware serial number, without spaces.</span></span>

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

### <span data-ttu-id="50a2a-122">-ErrorLogUri</span><span class="sxs-lookup"><span data-stu-id="50a2a-122">-ErrorLogUri</span></span>
<span data-ttu-id="50a2a-123">指向內含資料傳送操作之錯誤記錄的 blob 的 URI。</span><span class="sxs-lookup"><span data-stu-id="50a2a-123">A URI that points to the blob containing the error log for the data transfer operation.</span></span>

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

### <span data-ttu-id="50a2a-124">-ManifestFile</span><span class="sxs-lookup"><span data-stu-id="50a2a-124">-ManifestFile</span></span>
<span data-ttu-id="50a2a-125">磁碟機上資訊清單檔案的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="50a2a-125">The relative path of the manifest file on the drive.</span></span>

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

### <span data-ttu-id="50a2a-126">-ManifestHash</span><span class="sxs-lookup"><span data-stu-id="50a2a-126">-ManifestHash</span></span>
<span data-ttu-id="50a2a-127">磁片磁碟機上的資訊清單檔案的 Base16 編碼 MD5 雜湊值。</span><span class="sxs-lookup"><span data-stu-id="50a2a-127">The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>

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

### <span data-ttu-id="50a2a-128">-ManifestUri</span><span class="sxs-lookup"><span data-stu-id="50a2a-128">-ManifestUri</span></span>
<span data-ttu-id="50a2a-129">指向內含磁片磁碟機資訊清單檔案之 blob 的 URI。</span><span class="sxs-lookup"><span data-stu-id="50a2a-129">A URI that points to the blob containing the drive manifest file.</span></span>

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

### <span data-ttu-id="50a2a-130">-百分比</span><span class="sxs-lookup"><span data-stu-id="50a2a-130">-PercentComplete</span></span>
<span data-ttu-id="50a2a-131">已完成磁片磁碟機的百分比。</span><span class="sxs-lookup"><span data-stu-id="50a2a-131">Percentage completed for the drive.</span></span>

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

### <span data-ttu-id="50a2a-132">-State</span><span class="sxs-lookup"><span data-stu-id="50a2a-132">-State</span></span>
<span data-ttu-id="50a2a-133">磁片磁碟機的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="50a2a-133">The drive's current state.</span></span>

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

### <span data-ttu-id="50a2a-134">-VerboseLogUri</span><span class="sxs-lookup"><span data-stu-id="50a2a-134">-VerboseLogUri</span></span>
<span data-ttu-id="50a2a-135">指向內含資料傳輸作業詳細資料記錄之 blob 的 URI。</span><span class="sxs-lookup"><span data-stu-id="50a2a-135">A URI that points to the blob containing the verbose log for the data transfer operation.</span></span>

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

### <span data-ttu-id="50a2a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50a2a-136">CommonParameters</span></span>
<span data-ttu-id="50a2a-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="50a2a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50a2a-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="50a2a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50a2a-139">輸入</span><span class="sxs-lookup"><span data-stu-id="50a2a-139">INPUTS</span></span>

## <span data-ttu-id="50a2a-140">輸出</span><span class="sxs-lookup"><span data-stu-id="50a2a-140">OUTPUTS</span></span>

### <span data-ttu-id="50a2a-141">IDriveStatus （ImportExport）。 Api20161101。</span><span class="sxs-lookup"><span data-stu-id="50a2a-141">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus</span></span>

## <span data-ttu-id="50a2a-142">筆記</span><span class="sxs-lookup"><span data-stu-id="50a2a-142">NOTES</span></span>

<span data-ttu-id="50a2a-143">別名</span><span class="sxs-lookup"><span data-stu-id="50a2a-143">ALIASES</span></span>

## <span data-ttu-id="50a2a-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="50a2a-144">RELATED LINKS</span></span>

