---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: AzureRM.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storagesync/invoke-azurermstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StorageSync/Commands.StorageSync/help/Invoke-AzureRmStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StorageSync/Commands.StorageSync/help/Invoke-AzureRmStorageSyncCompatibilityCheck.md
ms.openlocfilehash: 73e0f00fe184a5462141b060717ca64567d4a67e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450143"
---
# <span data-ttu-id="df750-101">Invoke-AzureRmStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="df750-101">Invoke-AzureRmStorageSyncCompatibilityCheck</span></span>

## <span data-ttu-id="df750-102">摘要</span><span class="sxs-lookup"><span data-stu-id="df750-102">SYNOPSIS</span></span>
<span data-ttu-id="df750-103">檢查您的系統與 Azure 檔案同步處理之間可能的相容性問題。</span><span class="sxs-lookup"><span data-stu-id="df750-103">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df750-104">句法</span><span class="sxs-lookup"><span data-stu-id="df750-104">SYNTAX</span></span>

### <span data-ttu-id="df750-105">PathBased (預設) </span><span class="sxs-lookup"><span data-stu-id="df750-105">PathBased (Default)</span></span>
```
Invoke-AzureRmStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [-Quiet] [<CommonParameters>]
```

### <span data-ttu-id="df750-106">ComputerNameBased</span><span class="sxs-lookup"><span data-stu-id="df750-106">ComputerNameBased</span></span>
```
Invoke-AzureRmStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [-Quiet] [<CommonParameters>]
```

## <span data-ttu-id="df750-107">說明</span><span class="sxs-lookup"><span data-stu-id="df750-107">DESCRIPTION</span></span>
<span data-ttu-id="df750-108">**AzureRmStorageSyncCompatibilityCheck** Cmdlet 會檢查您的系統與 Azure 檔案同步處理之間可能的相容性問題。針對本機或遠端路徑，它會在系統和檔案命名空間上執行一組驗證，然後傳回它找到的任何相容性問題。</span><span class="sxs-lookup"><span data-stu-id="df750-108">The **Invoke-AzureRmStorageSyncCompatibilityCheck** cmdlet checks for potential compatibility issues between your system and Azure File Sync. Given a local or remote path, it performs a set of validations on the system and file namespace, and then returns any compatibility issues it finds.</span></span>
<span data-ttu-id="df750-109">系統檢查：</span><span class="sxs-lookup"><span data-stu-id="df750-109">System checks:</span></span>
- <span data-ttu-id="df750-110">OS 相容性檔案命名空間檢查：</span><span class="sxs-lookup"><span data-stu-id="df750-110">OS compatibility File namespace checks:</span></span>
- <span data-ttu-id="df750-111">不支援的字元</span><span class="sxs-lookup"><span data-stu-id="df750-111">Unsupported characters</span></span>
- <span data-ttu-id="df750-112">檔案大小上限</span><span class="sxs-lookup"><span data-stu-id="df750-112">Maximum file size</span></span>
- <span data-ttu-id="df750-113">最大路徑長度</span><span class="sxs-lookup"><span data-stu-id="df750-113">Maximum path length</span></span>
- <span data-ttu-id="df750-114">檔長度上限</span><span class="sxs-lookup"><span data-stu-id="df750-114">Maximum file length</span></span>
- <span data-ttu-id="df750-115">資料集大小上限</span><span class="sxs-lookup"><span data-stu-id="df750-115">Maximum dataset size</span></span>
- <span data-ttu-id="df750-116">目錄深度上限</span><span class="sxs-lookup"><span data-stu-id="df750-116">Maximum directory depth</span></span>

## <span data-ttu-id="df750-117">示例</span><span class="sxs-lookup"><span data-stu-id="df750-117">EXAMPLES</span></span>

### <span data-ttu-id="df750-118">範例1</span><span class="sxs-lookup"><span data-stu-id="df750-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA
```

<span data-ttu-id="df750-119">這個命令會檢查系統與 C:\DATA. 中的檔案和資料夾的相容性</span><span class="sxs-lookup"><span data-stu-id="df750-119">This command checks the compatibility of the system and also of files and folders in C:\DATA.</span></span>

### <span data-ttu-id="df750-120">範例2</span><span class="sxs-lookup"><span data-stu-id="df750-120">Example 2</span></span>
```powershell
PS C:\> Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

<span data-ttu-id="df750-121">這個命令會檢查 C:\DATA 中檔案和資料夾的相容性，但不會執行系統相容性檢查。</span><span class="sxs-lookup"><span data-stu-id="df750-121">This command checks the compatibility of files and folders in C:\DATA, but does not perform a system compatibility check.</span></span>

### <span data-ttu-id="df750-122">範例3</span><span class="sxs-lookup"><span data-stu-id="df750-122">Example 3</span></span>
```powershell
PS C:\> $errors = Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA
PS C:\> $errors | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results
```

<span data-ttu-id="df750-123">這個命令會檢查系統與 C:\DATA 中的檔案和資料夾相容性，然後將結果匯出為 CSV 檔案至 C:\results。</span><span class="sxs-lookup"><span data-stu-id="df750-123">This command checks the compatibility of the system and also of files and folders in C:\DATA, and then exports the results as a CSV file to C:\results.</span></span>

## <span data-ttu-id="df750-124">參數</span><span class="sxs-lookup"><span data-stu-id="df750-124">PARAMETERS</span></span>

### <span data-ttu-id="df750-125">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="df750-125">-ComputerName</span></span>
<span data-ttu-id="df750-126">您執行此檢查的電腦。</span><span class="sxs-lookup"><span data-stu-id="df750-126">The computer you are performing this check on.</span></span>

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

### <span data-ttu-id="df750-127">-認證</span><span class="sxs-lookup"><span data-stu-id="df750-127">-Credential</span></span>
<span data-ttu-id="df750-128">您要驗證之共用的認證。</span><span class="sxs-lookup"><span data-stu-id="df750-128">Your credentials for the share you are validating.</span></span>

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

### <span data-ttu-id="df750-129">-Path</span><span class="sxs-lookup"><span data-stu-id="df750-129">-Path</span></span>
<span data-ttu-id="df750-130">您要驗證之共用的 UNC 路徑。</span><span class="sxs-lookup"><span data-stu-id="df750-130">The UNC path of the share you are validating.</span></span>

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

### <span data-ttu-id="df750-131">-安靜</span><span class="sxs-lookup"><span data-stu-id="df750-131">-Quiet</span></span>
<span data-ttu-id="df750-132">取消將輸出報告寫入到主控台。</span><span class="sxs-lookup"><span data-stu-id="df750-132">Suppresses writing output report to console.</span></span>

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

### <span data-ttu-id="df750-133">-SkipNamespaceChecks</span><span class="sxs-lookup"><span data-stu-id="df750-133">-SkipNamespaceChecks</span></span>
<span data-ttu-id="df750-134">設定此標誌以略過檔案命名空間驗證，只執行系統驗證。</span><span class="sxs-lookup"><span data-stu-id="df750-134">Set this flag to skip file namespace validations and only perform system validations.</span></span>

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

### <span data-ttu-id="df750-135">-SkipSystemChecks</span><span class="sxs-lookup"><span data-stu-id="df750-135">-SkipSystemChecks</span></span>
<span data-ttu-id="df750-136">將此標誌設定為略過系統驗證，且只執行檔命名空間驗證。</span><span class="sxs-lookup"><span data-stu-id="df750-136">Set this flag to skip system validations and only perform file namespace validations.</span></span>

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

### <span data-ttu-id="df750-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df750-137">CommonParameters</span></span>
<span data-ttu-id="df750-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="df750-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df750-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="df750-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df750-140">輸入</span><span class="sxs-lookup"><span data-stu-id="df750-140">INPUTS</span></span>

### <span data-ttu-id="df750-141">所有</span><span class="sxs-lookup"><span data-stu-id="df750-141">None</span></span>

## <span data-ttu-id="df750-142">輸出</span><span class="sxs-lookup"><span data-stu-id="df750-142">OUTPUTS</span></span>

### <span data-ttu-id="df750-143">PSValidationResult 中的 StorageSync。</span><span class="sxs-lookup"><span data-stu-id="df750-143">Microsoft.Azure.Commands.StorageSync.Evaluation.Models.PSValidationResult</span></span>

## <span data-ttu-id="df750-144">筆記</span><span class="sxs-lookup"><span data-stu-id="df750-144">NOTES</span></span>
* <span data-ttu-id="df750-145">關鍵字： azure、azurerm、arm、資源、管理、storagesync、filesync</span><span class="sxs-lookup"><span data-stu-id="df750-145">Keywords: azure, azurerm, arm, resource, management, storagesync, filesync</span></span>

## <span data-ttu-id="df750-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="df750-146">RELATED LINKS</span></span>
