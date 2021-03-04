---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/powershell/module/az.importexport/new-AzImportExportDriveListObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
ms.openlocfilehash: 4b3907e71dd8d457b1ab38ecd5cdc82b38d7b772
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906629"
---
# <span data-ttu-id="61d67-101">New-AzImportExportDriveListObject</span><span class="sxs-lookup"><span data-stu-id="61d67-101">New-AzImportExportDriveListObject</span></span>

## <span data-ttu-id="61d67-102">簡介</span><span class="sxs-lookup"><span data-stu-id="61d67-102">SYNOPSIS</span></span>
<span data-ttu-id="61d67-103">建立 ImportExport 的 DriverList 物件。</span><span class="sxs-lookup"><span data-stu-id="61d67-103">Create a DriverList Object for ImportExport.</span></span>

## <span data-ttu-id="61d67-104">語法</span><span class="sxs-lookup"><span data-stu-id="61d67-104">SYNTAX</span></span>

```
New-AzImportExportDriveListObject [-BitLockerKey <String>] [-BytesSucceeded <Int64>] [-CopyStatus <String>]
 [-DriveHeaderHash <String>] [-DriveId <String>] [-ErrorLogUri <String>] [-ManifestFile <String>]
 [-ManifestHash <String>] [-ManifestUri <String>] [-PercentComplete <Int32>] [-State <DriveState>]
 [-VerboseLogUri <String>] [<CommonParameters>]
```

## <span data-ttu-id="61d67-105">描述</span><span class="sxs-lookup"><span data-stu-id="61d67-105">DESCRIPTION</span></span>
<span data-ttu-id="61d67-106">建立 ImportExport 的 DriverList 物件。</span><span class="sxs-lookup"><span data-stu-id="61d67-106">Create a DriverList Object for ImportExport.</span></span>

## <span data-ttu-id="61d67-107">例子</span><span class="sxs-lookup"><span data-stu-id="61d67-107">EXAMPLES</span></span>

### <span data-ttu-id="61d67-108">範例 1：為 ImportExport 工作建立新 DriveList</span><span class="sxs-lookup"><span data-stu-id="61d67-108">Example 1: Create a new DriveList for ImportExport job</span></span>
```powershell
PS C:\> New-AzImportExportDriveListObject -DriveId "9CA995BA" -BitLockerKey "238810-662376-448998-450120-652806-203390-606320-483076" -ManifestFile "\\DriveManifest.xml" -ManifestHash "109B21108597EF36D5785F08303F3638"

BitLockerKey                                            BytesSucceeded CopyStatus DriveHeaderHash DriveId  ErrorLogUri ManifestFile        ManifestHash                     ManifestUri PercentComplete State VerboseLogUri  
------------                                            -------------- ---------- --------------- -------  ----------- ------------        ------------                     ----------- --------------- ----- ------- 
238810-662376-448998-450120-652806-203390-606320-483076 0                                         9CA995BA             \\DriveManifest.xml 109B21108597EF36D5785F08303F3638             0
```

<span data-ttu-id="61d67-109">這些 Cmdlet 會為 ImportExport 工作建立一個新的 DriveList。</span><span class="sxs-lookup"><span data-stu-id="61d67-109">These cmdlets create a new DriveList for ImportExport job.</span></span>

## <span data-ttu-id="61d67-110">參數</span><span class="sxs-lookup"><span data-stu-id="61d67-110">PARAMETERS</span></span>

### <span data-ttu-id="61d67-111">-BitLockerKey</span><span class="sxs-lookup"><span data-stu-id="61d67-111">-BitLockerKey</span></span>
<span data-ttu-id="61d67-112">用來加密硬碟的 BitLocker 金鑰。</span><span class="sxs-lookup"><span data-stu-id="61d67-112">The BitLocker key used to encrypt the drive.</span></span>

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

### <span data-ttu-id="61d67-113">-BytesSuced</span><span class="sxs-lookup"><span data-stu-id="61d67-113">-BytesSucceeded</span></span>
<span data-ttu-id="61d67-114">已成功傳輸硬碟的位元組。</span><span class="sxs-lookup"><span data-stu-id="61d67-114">Bytes successfully transferred for the drive.</span></span>

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

### <span data-ttu-id="61d67-115">-CopyStatus</span><span class="sxs-lookup"><span data-stu-id="61d67-115">-CopyStatus</span></span>
<span data-ttu-id="61d67-116">資料傳輸程式的詳細狀態。</span><span class="sxs-lookup"><span data-stu-id="61d67-116">Detailed status about the data transfer process.</span></span>
<span data-ttu-id="61d67-117">在磁碟機位於傳輸狀態之前，此欄位不會在回應中返回。</span><span class="sxs-lookup"><span data-stu-id="61d67-117">This field is not returned in the response until the drive is in the Transferring state.</span></span>

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

### <span data-ttu-id="61d67-118">-DriveHeaderHash</span><span class="sxs-lookup"><span data-stu-id="61d67-118">-DriveHeaderHash</span></span>
<span data-ttu-id="61d67-119">磁碟機頭雜湊值。</span><span class="sxs-lookup"><span data-stu-id="61d67-119">The drive header hash value.</span></span>

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

### <span data-ttu-id="61d67-120">-DriveId</span><span class="sxs-lookup"><span data-stu-id="61d67-120">-DriveId</span></span>
<span data-ttu-id="61d67-121">硬碟的硬體序號，不含空格。</span><span class="sxs-lookup"><span data-stu-id="61d67-121">The drive's hardware serial number, without spaces.</span></span>

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

### <span data-ttu-id="61d67-122">-ErrorLogUri</span><span class="sxs-lookup"><span data-stu-id="61d67-122">-ErrorLogUri</span></span>
<span data-ttu-id="61d67-123">指向包含資料傳輸作業錯誤記錄之 Blob 的 URI。</span><span class="sxs-lookup"><span data-stu-id="61d67-123">A URI that points to the blob containing the error log for the data transfer operation.</span></span>

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

### <span data-ttu-id="61d67-124">-ManifestFile</span><span class="sxs-lookup"><span data-stu-id="61d67-124">-ManifestFile</span></span>
<span data-ttu-id="61d67-125">硬碟上之清單檔案的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="61d67-125">The relative path of the manifest file on the drive.</span></span>

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

### <span data-ttu-id="61d67-126">-ManifestHash</span><span class="sxs-lookup"><span data-stu-id="61d67-126">-ManifestHash</span></span>
<span data-ttu-id="61d67-127">雲端硬碟上清單檔案的 Base16 編碼 MD5 雜湊。</span><span class="sxs-lookup"><span data-stu-id="61d67-127">The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>

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

### <span data-ttu-id="61d67-128">-ManifestUri</span><span class="sxs-lookup"><span data-stu-id="61d67-128">-ManifestUri</span></span>
<span data-ttu-id="61d67-129">指向包含磁碟機清單檔案之 Blob 的 URI。</span><span class="sxs-lookup"><span data-stu-id="61d67-129">A URI that points to the blob containing the drive manifest file.</span></span>

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

### <span data-ttu-id="61d67-130">-完成百分比</span><span class="sxs-lookup"><span data-stu-id="61d67-130">-PercentComplete</span></span>
<span data-ttu-id="61d67-131">已完成的磁碟機百分比。</span><span class="sxs-lookup"><span data-stu-id="61d67-131">Percentage completed for the drive.</span></span>

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

### <span data-ttu-id="61d67-132">-State</span><span class="sxs-lookup"><span data-stu-id="61d67-132">-State</span></span>
<span data-ttu-id="61d67-133">磁碟機的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="61d67-133">The drive's current state.</span></span>

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

### <span data-ttu-id="61d67-134">-VerboseLogUri</span><span class="sxs-lookup"><span data-stu-id="61d67-134">-VerboseLogUri</span></span>
<span data-ttu-id="61d67-135">指向包含資料傳輸作業詳細記錄之 Blob 的 URI。</span><span class="sxs-lookup"><span data-stu-id="61d67-135">A URI that points to the blob containing the verbose log for the data transfer operation.</span></span>

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

### <span data-ttu-id="61d67-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61d67-136">CommonParameters</span></span>
<span data-ttu-id="61d67-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="61d67-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61d67-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="61d67-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61d67-139">輸入</span><span class="sxs-lookup"><span data-stu-id="61d67-139">INPUTS</span></span>

## <span data-ttu-id="61d67-140">輸出</span><span class="sxs-lookup"><span data-stu-id="61d67-140">OUTPUTS</span></span>

### <span data-ttu-id="61d67-141">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.models.Api20161101.IDriveStatus</span><span class="sxs-lookup"><span data-stu-id="61d67-141">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus</span></span>

## <span data-ttu-id="61d67-142">筆記</span><span class="sxs-lookup"><span data-stu-id="61d67-142">NOTES</span></span>

<span data-ttu-id="61d67-143">別名</span><span class="sxs-lookup"><span data-stu-id="61d67-143">ALIASES</span></span>

## <span data-ttu-id="61d67-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="61d67-144">RELATED LINKS</span></span>

