---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: FB9ACBA2-081E-4876-A21A-F5BA11CBEDA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/publish-azurermvmdscconfiguration
schema: 2.0.0
ms.openlocfilehash: c9a778638a0ca86198079227cfa0021a96ac138b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801754"
---
# <span data-ttu-id="f7237-101">Publish-AzureRmVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f7237-101">Publish-AzureRmVMDscConfiguration</span></span>

## <span data-ttu-id="f7237-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f7237-102">SYNOPSIS</span></span>
<span data-ttu-id="f7237-103">將 DSC 腳本上傳到 Azure blob 儲存空間。</span><span class="sxs-lookup"><span data-stu-id="f7237-103">Uploads a DSC script to Azure blob storage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7237-104">句法</span><span class="sxs-lookup"><span data-stu-id="f7237-104">SYNTAX</span></span>

### <span data-ttu-id="f7237-105">UploadArchive (預設) </span><span class="sxs-lookup"><span data-stu-id="f7237-105">UploadArchive (Default)</span></span>
```
Publish-AzureRmVMDscConfiguration [-ResourceGroupName] <String> [-ConfigurationPath] <String>
 [[-ContainerName] <String>] [-StorageAccountName] <String> [-StorageEndpointSuffix <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7237-106">CreateArchive</span><span class="sxs-lookup"><span data-stu-id="f7237-106">CreateArchive</span></span>
```
Publish-AzureRmVMDscConfiguration [-ConfigurationPath] <String> [[-OutputArchivePath] <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7237-107">說明</span><span class="sxs-lookup"><span data-stu-id="f7237-107">DESCRIPTION</span></span>
<span data-ttu-id="f7237-108">**AzureRmVMDscConfiguration** Cmdlet 會將所需的狀態設定上傳到 azure blob 儲存空間)  (，稍後就可以使用 Set-AzureRmVMDscExtension Cmdlet 將它套用至 azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="f7237-108">The **Publish-AzureRmVMDscConfiguration** cmdlet uploads a Desired State Configuration (DSC) script to Azure blob storage, which later can be applied to Azure virtual machines using the Set-AzureRmVMDscExtension cmdlet.</span></span>

## <span data-ttu-id="f7237-109">示例</span><span class="sxs-lookup"><span data-stu-id="f7237-109">EXAMPLES</span></span>

### <span data-ttu-id="f7237-110">範例1：建立 .zip 封裝，將其上傳到 Azure 儲存空間</span><span class="sxs-lookup"><span data-stu-id="f7237-110">Example 1: Create a .zip package an upload it to Azure storage</span></span>
```
PS C:\> Publish-AzureRmVMDscConfiguration ".\MyConfiguration.ps1"
```

<span data-ttu-id="f7237-111">這個命令會針對指定的腳本及任何相依資源模組建立 .zip 套件，並將其上傳到 Azure 儲存空間。</span><span class="sxs-lookup"><span data-stu-id="f7237-111">This command creates a .zip package for the given script and any dependent resource modules and uploads it to Azure storage.</span></span>

### <span data-ttu-id="f7237-112">範例2：建立 .zip 封裝並將它儲存至本機檔案</span><span class="sxs-lookup"><span data-stu-id="f7237-112">Example 2: Create a .zip package and store it to a local file</span></span>
```
PS C:\> Publish-AzureRmVMDscConfiguration ".\MyConfiguration.ps1" -OutputArchivePath ".\MyConfiguration.ps1.zip"
```

<span data-ttu-id="f7237-113">這個命令會針對指定的腳本及任何相依資源模組建立 .zip 套件，並將其儲存在名為 .\MyConfiguration.ps1.zip 的本機檔案中。</span><span class="sxs-lookup"><span data-stu-id="f7237-113">This command creates a .zip package for the given script and any dependent resource modules and stores it in the local file that is named .\MyConfiguration.ps1.zip.</span></span>

### <span data-ttu-id="f7237-114">範例3：新增配置至封存，然後上傳至儲存空間</span><span class="sxs-lookup"><span data-stu-id="f7237-114">Example 3: Add configuration to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzureRmVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -SkipDependencyDetection
```

<span data-ttu-id="f7237-115">這個命令會將名為 Sample.ps1 的設定新增到設定封存，以上傳至 Azure 儲存空間，並跳過相依資源模組。</span><span class="sxs-lookup"><span data-stu-id="f7237-115">This command adds configuration named Sample.ps1 to the configuration archive to upload to Azure storage and skips dependent resource modules.</span></span>

### <span data-ttu-id="f7237-116">範例4：將配置和設定資料新增到封存，然後上傳至 [儲存空間]</span><span class="sxs-lookup"><span data-stu-id="f7237-116">Example 4: Add configuration and configuration data to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzureRmVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -ConfigurationDataPath "C:\SampleData.psd1"
```

<span data-ttu-id="f7237-117">這個命令會將名為 SampleData.psd1 的配置 Sample.ps1 和設定資料，新增至要上傳至 Azure 儲存空間的設定封存。</span><span class="sxs-lookup"><span data-stu-id="f7237-117">This command adds configuration named Sample.ps1 and configuration data named SampleData.psd1 to the configuration archive to upload to Azure storage.</span></span>

### <span data-ttu-id="f7237-118">範例5：將配置、設定資料及其他內容新增到封存，然後上傳至儲存空間</span><span class="sxs-lookup"><span data-stu-id="f7237-118">Example 5: Add configuration, configuration data, and additional content to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzureRmVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -AdditionalPath @("C:\ContentDir1", "C:\File.txt") -ConfigurationDataPath "C:\SampleData.psd1"
```

<span data-ttu-id="f7237-119">這個命令會將名為 Sample.ps1、設定資料 SampleData.psd1 的設定，以及要上傳至 Azure 儲存空間的其他內容。</span><span class="sxs-lookup"><span data-stu-id="f7237-119">This command adds configuration named Sample.ps1, configuration data SampleData.psd1, and additional content to configuration archive to upload to Azure storage.</span></span>

## <span data-ttu-id="f7237-120">參數</span><span class="sxs-lookup"><span data-stu-id="f7237-120">PARAMETERS</span></span>

### <span data-ttu-id="f7237-121">-AdditionalPath</span><span class="sxs-lookup"><span data-stu-id="f7237-121">-AdditionalPath</span></span>
<span data-ttu-id="f7237-122">指定要包含在配置封存的檔案或目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="f7237-122">Specifies the path of a file or a directory to include in the configuration archive.</span></span>
<span data-ttu-id="f7237-123">它會與設定一起下載到虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="f7237-123">It gets downloaded to the virtual machine together with the configuration.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7237-124">-ConfigurationDataPath</span><span class="sxs-lookup"><span data-stu-id="f7237-124">-ConfigurationDataPath</span></span>
<span data-ttu-id="f7237-125">指定 psd1 檔案的路徑，該檔案會指定設定的資料。</span><span class="sxs-lookup"><span data-stu-id="f7237-125">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>
<span data-ttu-id="f7237-126">這會新增到 [設定] 封存，然後傳遞到 [設定] 函式。</span><span class="sxs-lookup"><span data-stu-id="f7237-126">This is added to the configuration archive and then passed to the configuration function.</span></span>
<span data-ttu-id="f7237-127">透過 Set-AzureRmVMDscExtension Cmdlet 提供的配置資料路徑會覆寫它</span><span class="sxs-lookup"><span data-stu-id="f7237-127">It gets overwritten by the configuration data path provided through the Set-AzureRmVMDscExtension cmdlet</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7237-128">-ConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="f7237-128">-ConfigurationPath</span></span>
<span data-ttu-id="f7237-129">指定包含一或多個設定的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="f7237-129">Specifies the path of a file that contains one or more configurations.</span></span>
<span data-ttu-id="f7237-130">檔案可以是 Windows PowerShell 腳本 (. ps1) 檔案或 Windows PowerShell 模組 ( psm1) 檔案。</span><span class="sxs-lookup"><span data-stu-id="f7237-130">The file can be a Windows PowerShell script (.ps1) file or a Windows PowerShell module (.psm1) file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7237-131">-容器</span><span class="sxs-lookup"><span data-stu-id="f7237-131">-ContainerName</span></span>
<span data-ttu-id="f7237-132">指定要上傳配置的 Azure 存儲容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="f7237-132">Specifies the name of the Azure storage container the configuration is uploaded to.</span></span>

```yaml
Type: String
Parameter Sets: UploadArchive
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7237-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7237-133">-DefaultProfile</span></span>
<span data-ttu-id="f7237-134">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f7237-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7237-135">-Force</span><span class="sxs-lookup"><span data-stu-id="f7237-135">-Force</span></span>
<span data-ttu-id="f7237-136">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="f7237-136">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7237-137">-OutputArchivePath</span><span class="sxs-lookup"><span data-stu-id="f7237-137">-OutputArchivePath</span></span>
<span data-ttu-id="f7237-138">指定要寫入配置封存的本機 .zip 檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="f7237-138">Specifies the path of a local .zip file to write the configuration archive to.</span></span>
<span data-ttu-id="f7237-139">使用此參數時，不會將配置腳本上傳到 Azure blob 儲存空間。</span><span class="sxs-lookup"><span data-stu-id="f7237-139">When this parameter is used, the configuration script is not uploaded to Azure blob storage.</span></span>

```yaml
Type: String
Parameter Sets: CreateArchive
Aliases: ConfigurationArchivePath

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7237-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7237-140">-ResourceGroupName</span></span>
<span data-ttu-id="f7237-141">指定包含儲存空間帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f7237-141">Specifies the name of the resource group that contains the storage account.</span></span>

```yaml
Type: String
Parameter Sets: UploadArchive
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7237-142">-SkipDependencyDetection</span><span class="sxs-lookup"><span data-stu-id="f7237-142">-SkipDependencyDetection</span></span>
<span data-ttu-id="f7237-143">表示此 Cmdlet 排除來自配置封存的 DSC 資源相依性。</span><span class="sxs-lookup"><span data-stu-id="f7237-143">Indicates that this cmdlet excludes DSC resource dependencies from the configuration archive.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7237-144">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f7237-144">-StorageAccountName</span></span>
<span data-ttu-id="f7237-145">指定 Azure 儲存空間帳戶名稱，該名稱是用來將設定腳本上傳到由 *容器* 參數指定的容器。</span><span class="sxs-lookup"><span data-stu-id="f7237-145">Specifies the Azure storage account name that is used to upload the configuration script to the container specified by the *ContainerName* parameter.</span></span>

```yaml
Type: String
Parameter Sets: UploadArchive
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7237-146">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="f7237-146">-StorageEndpointSuffix</span></span>
<span data-ttu-id="f7237-147">指定存儲端點的尾碼。</span><span class="sxs-lookup"><span data-stu-id="f7237-147">Specifies the suffix for the storage end point.</span></span>

```yaml
Type: String
Parameter Sets: UploadArchive
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7237-148">-確認</span><span class="sxs-lookup"><span data-stu-id="f7237-148">-Confirm</span></span>
<span data-ttu-id="f7237-149">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f7237-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7237-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7237-150">-WhatIf</span></span>
<span data-ttu-id="f7237-151">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f7237-151">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="f7237-152">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f7237-152">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7237-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7237-153">CommonParameters</span></span>
<span data-ttu-id="f7237-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f7237-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7237-155">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f7237-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7237-156">輸入</span><span class="sxs-lookup"><span data-stu-id="f7237-156">INPUTS</span></span>

### <span data-ttu-id="f7237-157">字串</span><span class="sxs-lookup"><span data-stu-id="f7237-157">String</span></span>
<span data-ttu-id="f7237-158">"ConfigurationPath" 參數從管線接受類型 "String" 的值</span><span class="sxs-lookup"><span data-stu-id="f7237-158">Parameter 'ConfigurationPath' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="f7237-159">輸出</span><span class="sxs-lookup"><span data-stu-id="f7237-159">OUTPUTS</span></span>

### <span data-ttu-id="f7237-160">System.object</span><span class="sxs-lookup"><span data-stu-id="f7237-160">System.String</span></span>

## <span data-ttu-id="f7237-161">筆記</span><span class="sxs-lookup"><span data-stu-id="f7237-161">NOTES</span></span>

## <span data-ttu-id="f7237-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="f7237-162">RELATED LINKS</span></span>

[<span data-ttu-id="f7237-163">AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="f7237-163">Get-AzureRmVMDscExtension</span></span>](./Get-AzureRmVMDscExtension.md)

[<span data-ttu-id="f7237-164">移除-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="f7237-164">Remove-AzureRmVMDscExtension</span></span>](./Remove-AzureRmVMDscExtension.md)

[<span data-ttu-id="f7237-165">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="f7237-165">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


