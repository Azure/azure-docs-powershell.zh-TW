---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/az.storagesync/invoke-azstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
ms.openlocfilehash: b6052172ecca2821b1373d93a8de870969a6b4f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915006"
---
# <span data-ttu-id="8755c-101">Invoke-AzStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="8755c-101">Invoke-AzStorageSyncCompatibilityCheck</span></span>

## <span data-ttu-id="8755c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8755c-102">SYNOPSIS</span></span>
<span data-ttu-id="8755c-103">檢查系統與 Azure 檔案同步處理之間潛在的相容性問題。</span><span class="sxs-lookup"><span data-stu-id="8755c-103">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

## <span data-ttu-id="8755c-104">語法</span><span class="sxs-lookup"><span data-stu-id="8755c-104">SYNTAX</span></span>

### <span data-ttu-id="8755c-105">PathBased (預設) </span><span class="sxs-lookup"><span data-stu-id="8755c-105">PathBased (Default)</span></span>
```
Invoke-AzStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [<CommonParameters>]
```

### <span data-ttu-id="8755c-106">ComputerNameBased</span><span class="sxs-lookup"><span data-stu-id="8755c-106">ComputerNameBased</span></span>
```
Invoke-AzStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [<CommonParameters>]
```

## <span data-ttu-id="8755c-107">描述</span><span class="sxs-lookup"><span data-stu-id="8755c-107">DESCRIPTION</span></span>
<span data-ttu-id="8755c-108">**Invoke-AzStorageSyncCompatibilityCheck** Cmdlet 會檢查系統與 Azure 檔案同步處理之間潛在的相容性問題。如果為本地或遠端路徑，它會在系統與檔案命名空間上執行一組驗證，然後會返回找到的任何相容性問題。</span><span class="sxs-lookup"><span data-stu-id="8755c-108">The **Invoke-AzStorageSyncCompatibilityCheck** cmdlet checks for potential compatibility issues between your system and Azure File Sync. Given a local or remote path, it performs a set of validations on the system and file namespace, and then returns any compatibility issues it finds.</span></span>
<span data-ttu-id="8755c-109">系統檢查：</span><span class="sxs-lookup"><span data-stu-id="8755c-109">System checks:</span></span>
- <span data-ttu-id="8755c-110">OS 相容性檔案命名空間檢查：</span><span class="sxs-lookup"><span data-stu-id="8755c-110">OS compatibility File namespace checks:</span></span>
- <span data-ttu-id="8755c-111">不支援的字元</span><span class="sxs-lookup"><span data-stu-id="8755c-111">Unsupported characters</span></span>
- <span data-ttu-id="8755c-112">檔案大小上限</span><span class="sxs-lookup"><span data-stu-id="8755c-112">Maximum file size</span></span>
- <span data-ttu-id="8755c-113">路徑長度上限</span><span class="sxs-lookup"><span data-stu-id="8755c-113">Maximum path length</span></span>
- <span data-ttu-id="8755c-114">檔案長度上限</span><span class="sxs-lookup"><span data-stu-id="8755c-114">Maximum file length</span></span>
- <span data-ttu-id="8755c-115">資料集大小上限</span><span class="sxs-lookup"><span data-stu-id="8755c-115">Maximum dataset size</span></span>
- <span data-ttu-id="8755c-116">目錄深度上限</span><span class="sxs-lookup"><span data-stu-id="8755c-116">Maximum directory depth</span></span>

## <span data-ttu-id="8755c-117">例子</span><span class="sxs-lookup"><span data-stu-id="8755c-117">EXAMPLES</span></span>

### <span data-ttu-id="8755c-118">範例 1</span><span class="sxs-lookup"><span data-stu-id="8755c-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA
```

<span data-ttu-id="8755c-119">此命令會檢查系統以及 C：\DATA 中檔案和資料夾的相容性。</span><span class="sxs-lookup"><span data-stu-id="8755c-119">This command checks the compatibility of the system and also of files and folders in C:\DATA.</span></span>

### <span data-ttu-id="8755c-120">範例 2</span><span class="sxs-lookup"><span data-stu-id="8755c-120">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

<span data-ttu-id="8755c-121">此命令會檢查 C：\DATA 中檔案和資料夾的相容性，但不執行系統相容性檢查。</span><span class="sxs-lookup"><span data-stu-id="8755c-121">This command checks the compatibility of files and folders in C:\DATA, but does not perform a system compatibility check.</span></span>

### <span data-ttu-id="8755c-122">範例 3</span><span class="sxs-lookup"><span data-stu-id="8755c-122">Example 3</span></span>
```powershell
PS C:\> $validation = Invoke-AzStorageSyncCompatibilityCheck C:\DATA
PS C:\> $validation.Results | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results.csv -Encoding utf8
```

<span data-ttu-id="8755c-123">此命令會檢查系統以及 C：\DATA 中檔案和資料夾的相容性，然後將結果匯出為 CSV 檔案至 C：\results。</span><span class="sxs-lookup"><span data-stu-id="8755c-123">This command checks the compatibility of the system and also of files and folders in C:\DATA, and then exports the results as a CSV file to C:\results.</span></span>

## <span data-ttu-id="8755c-124">參數</span><span class="sxs-lookup"><span data-stu-id="8755c-124">PARAMETERS</span></span>

### <span data-ttu-id="8755c-125">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="8755c-125">-ComputerName</span></span>
<span data-ttu-id="8755c-126">您執行此檢查的電腦。</span><span class="sxs-lookup"><span data-stu-id="8755c-126">The computer you are performing this check on.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputerNameBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8755c-127">-認證</span><span class="sxs-lookup"><span data-stu-id="8755c-127">-Credential</span></span>
<span data-ttu-id="8755c-128">您驗證之共用之認證。</span><span class="sxs-lookup"><span data-stu-id="8755c-128">Your credentials for the share you are validating.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8755c-129">-路徑</span><span class="sxs-lookup"><span data-stu-id="8755c-129">-Path</span></span>
<span data-ttu-id="8755c-130">您驗證之共用之 UNC 路徑。</span><span class="sxs-lookup"><span data-stu-id="8755c-130">The UNC path of the share you are validating.</span></span>

```yaml
Type: System.String
Parameter Sets: PathBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8755c-131">-SkipNamespaceChecks</span><span class="sxs-lookup"><span data-stu-id="8755c-131">-SkipNamespaceChecks</span></span>
<span data-ttu-id="8755c-132">設定此標號以略過檔案命名空間驗證，只執行系統驗證。</span><span class="sxs-lookup"><span data-stu-id="8755c-132">Set this flag to skip file namespace validations and only perform system validations.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PathBased
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8755c-133">-SkipSystemChecks</span><span class="sxs-lookup"><span data-stu-id="8755c-133">-SkipSystemChecks</span></span>
<span data-ttu-id="8755c-134">設定此標號以略過系統驗證，只執行檔案命名空間驗證。</span><span class="sxs-lookup"><span data-stu-id="8755c-134">Set this flag to skip system validations and only perform file namespace validations.</span></span>

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

### <span data-ttu-id="8755c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8755c-135">CommonParameters</span></span>
<span data-ttu-id="8755c-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8755c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8755c-137">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="8755c-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8755c-138">輸入</span><span class="sxs-lookup"><span data-stu-id="8755c-138">INPUTS</span></span>

### <span data-ttu-id="8755c-139">沒有</span><span class="sxs-lookup"><span data-stu-id="8755c-139">None</span></span>

## <span data-ttu-id="8755c-140">輸出</span><span class="sxs-lookup"><span data-stu-id="8755c-140">OUTPUTS</span></span>

### <span data-ttu-id="8755c-141">Microsoft.Azure.Commands.storageSync.evaluation.models.PSValidationResult</span><span class="sxs-lookup"><span data-stu-id="8755c-141">Microsoft.Azure.Commands.StorageSync.Evaluation.Models.PSValidationResult</span></span>

## <span data-ttu-id="8755c-142">筆記</span><span class="sxs-lookup"><span data-stu-id="8755c-142">NOTES</span></span>
* <span data-ttu-id="8755c-143">關鍵字：azure、Az、arm、resource、management、storagesync、filesync</span><span class="sxs-lookup"><span data-stu-id="8755c-143">Keywords: azure, Az, arm, resource, management, storagesync, filesync</span></span>

## <span data-ttu-id="8755c-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="8755c-144">RELATED LINKS</span></span>
