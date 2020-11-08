---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
ms.openlocfilehash: 51882269c342e766a3b714f931486eca437b9e58
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129725"
---
# <span data-ttu-id="143a5-101">Invoke-AzStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="143a5-101">Invoke-AzStorageSyncCompatibilityCheck</span></span>

## <span data-ttu-id="143a5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="143a5-102">SYNOPSIS</span></span>
<span data-ttu-id="143a5-103">檢查您的系統與 Azure 檔案同步處理之間可能的相容性問題。</span><span class="sxs-lookup"><span data-stu-id="143a5-103">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

## <span data-ttu-id="143a5-104">句法</span><span class="sxs-lookup"><span data-stu-id="143a5-104">SYNTAX</span></span>

### <span data-ttu-id="143a5-105">PathBased (預設) </span><span class="sxs-lookup"><span data-stu-id="143a5-105">PathBased (Default)</span></span>
```
Invoke-AzStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [<CommonParameters>]
```

### <span data-ttu-id="143a5-106">ComputerNameBased</span><span class="sxs-lookup"><span data-stu-id="143a5-106">ComputerNameBased</span></span>
```
Invoke-AzStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [<CommonParameters>]
```

## <span data-ttu-id="143a5-107">說明</span><span class="sxs-lookup"><span data-stu-id="143a5-107">DESCRIPTION</span></span>
<span data-ttu-id="143a5-108">**AzStorageSyncCompatibilityCheck** Cmdlet 會檢查您的系統與 Azure 檔案同步處理之間可能的相容性問題。針對本機或遠端路徑，它會在系統和檔案命名空間上執行一組驗證，然後傳回它找到的任何相容性問題。</span><span class="sxs-lookup"><span data-stu-id="143a5-108">The **Invoke-AzStorageSyncCompatibilityCheck** cmdlet checks for potential compatibility issues between your system and Azure File Sync. Given a local or remote path, it performs a set of validations on the system and file namespace, and then returns any compatibility issues it finds.</span></span>
<span data-ttu-id="143a5-109">系統檢查：</span><span class="sxs-lookup"><span data-stu-id="143a5-109">System checks:</span></span>
- <span data-ttu-id="143a5-110">OS 相容性檔案命名空間檢查：</span><span class="sxs-lookup"><span data-stu-id="143a5-110">OS compatibility File namespace checks:</span></span>
- <span data-ttu-id="143a5-111">不支援的字元</span><span class="sxs-lookup"><span data-stu-id="143a5-111">Unsupported characters</span></span>
- <span data-ttu-id="143a5-112">檔案大小上限</span><span class="sxs-lookup"><span data-stu-id="143a5-112">Maximum file size</span></span>
- <span data-ttu-id="143a5-113">最大路徑長度</span><span class="sxs-lookup"><span data-stu-id="143a5-113">Maximum path length</span></span>
- <span data-ttu-id="143a5-114">檔長度上限</span><span class="sxs-lookup"><span data-stu-id="143a5-114">Maximum file length</span></span>
- <span data-ttu-id="143a5-115">資料集大小上限</span><span class="sxs-lookup"><span data-stu-id="143a5-115">Maximum dataset size</span></span>
- <span data-ttu-id="143a5-116">目錄深度上限</span><span class="sxs-lookup"><span data-stu-id="143a5-116">Maximum directory depth</span></span>

## <span data-ttu-id="143a5-117">示例</span><span class="sxs-lookup"><span data-stu-id="143a5-117">EXAMPLES</span></span>

### <span data-ttu-id="143a5-118">範例1</span><span class="sxs-lookup"><span data-stu-id="143a5-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA
```

<span data-ttu-id="143a5-119">這個命令會檢查系統與 C:\DATA. 中的檔案和資料夾的相容性</span><span class="sxs-lookup"><span data-stu-id="143a5-119">This command checks the compatibility of the system and also of files and folders in C:\DATA.</span></span>

### <span data-ttu-id="143a5-120">範例2</span><span class="sxs-lookup"><span data-stu-id="143a5-120">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

<span data-ttu-id="143a5-121">這個命令會檢查 C:\DATA 中檔案和資料夾的相容性，但不會執行系統相容性檢查。</span><span class="sxs-lookup"><span data-stu-id="143a5-121">This command checks the compatibility of files and folders in C:\DATA, but does not perform a system compatibility check.</span></span>

### <span data-ttu-id="143a5-122">範例3</span><span class="sxs-lookup"><span data-stu-id="143a5-122">Example 3</span></span>
```powershell
PS C:\> $validation = Invoke-AzStorageSyncCompatibilityCheck C:\DATA
PS C:\> $validation.Results | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results.csv -Encoding utf8
```

<span data-ttu-id="143a5-123">這個命令會檢查系統與 C:\DATA 中的檔案和資料夾相容性，然後將結果匯出為 CSV 檔案至 C:\results。</span><span class="sxs-lookup"><span data-stu-id="143a5-123">This command checks the compatibility of the system and also of files and folders in C:\DATA, and then exports the results as a CSV file to C:\results.</span></span>

## <span data-ttu-id="143a5-124">參數</span><span class="sxs-lookup"><span data-stu-id="143a5-124">PARAMETERS</span></span>

### <span data-ttu-id="143a5-125">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="143a5-125">-ComputerName</span></span>
<span data-ttu-id="143a5-126">您執行此檢查的電腦。</span><span class="sxs-lookup"><span data-stu-id="143a5-126">The computer you are performing this check on.</span></span>

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

### <span data-ttu-id="143a5-127">-認證</span><span class="sxs-lookup"><span data-stu-id="143a5-127">-Credential</span></span>
<span data-ttu-id="143a5-128">您要驗證之共用的認證。</span><span class="sxs-lookup"><span data-stu-id="143a5-128">Your credentials for the share you are validating.</span></span>

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

### <span data-ttu-id="143a5-129">-Path</span><span class="sxs-lookup"><span data-stu-id="143a5-129">-Path</span></span>
<span data-ttu-id="143a5-130">您要驗證之共用的 UNC 路徑。</span><span class="sxs-lookup"><span data-stu-id="143a5-130">The UNC path of the share you are validating.</span></span>

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

### <span data-ttu-id="143a5-131">-SkipNamespaceChecks</span><span class="sxs-lookup"><span data-stu-id="143a5-131">-SkipNamespaceChecks</span></span>
<span data-ttu-id="143a5-132">設定此標誌以略過檔案命名空間驗證，只執行系統驗證。</span><span class="sxs-lookup"><span data-stu-id="143a5-132">Set this flag to skip file namespace validations and only perform system validations.</span></span>

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

### <span data-ttu-id="143a5-133">-SkipSystemChecks</span><span class="sxs-lookup"><span data-stu-id="143a5-133">-SkipSystemChecks</span></span>
<span data-ttu-id="143a5-134">將此標誌設定為略過系統驗證，且只執行檔命名空間驗證。</span><span class="sxs-lookup"><span data-stu-id="143a5-134">Set this flag to skip system validations and only perform file namespace validations.</span></span>

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

### <span data-ttu-id="143a5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="143a5-135">CommonParameters</span></span>
<span data-ttu-id="143a5-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="143a5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="143a5-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="143a5-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="143a5-138">輸入</span><span class="sxs-lookup"><span data-stu-id="143a5-138">INPUTS</span></span>

### <span data-ttu-id="143a5-139">所有</span><span class="sxs-lookup"><span data-stu-id="143a5-139">None</span></span>

## <span data-ttu-id="143a5-140">輸出</span><span class="sxs-lookup"><span data-stu-id="143a5-140">OUTPUTS</span></span>

### <span data-ttu-id="143a5-141">PSValidationResult 中的 StorageSync。</span><span class="sxs-lookup"><span data-stu-id="143a5-141">Microsoft.Azure.Commands.StorageSync.Evaluation.Models.PSValidationResult</span></span>

## <span data-ttu-id="143a5-142">筆記</span><span class="sxs-lookup"><span data-stu-id="143a5-142">NOTES</span></span>
* <span data-ttu-id="143a5-143">關鍵字： azure、Az、arm、資源、管理、storagesync、filesync</span><span class="sxs-lookup"><span data-stu-id="143a5-143">Keywords: azure, Az, arm, resource, management, storagesync, filesync</span></span>

## <span data-ttu-id="143a5-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="143a5-144">RELATED LINKS</span></span>
