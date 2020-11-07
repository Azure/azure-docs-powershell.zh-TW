---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5490BB24-127E-4C21-B85F-B70D817B659A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/save-azdatafactorylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
ms.openlocfilehash: 19d2c5c9b03b08bd31839dfe7e072de9517ff459
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788114"
---
# <span data-ttu-id="df894-101">Save-AzDataFactoryLog</span><span class="sxs-lookup"><span data-stu-id="df894-101">Save-AzDataFactoryLog</span></span>

## <span data-ttu-id="df894-102">摘要</span><span class="sxs-lookup"><span data-stu-id="df894-102">SYNOPSIS</span></span>
<span data-ttu-id="df894-103">從 Azure HDInsight 處理下載記錄檔。</span><span class="sxs-lookup"><span data-stu-id="df894-103">Downloads log files from Azure HDInsight processing.</span></span>

## <span data-ttu-id="df894-104">句法</span><span class="sxs-lookup"><span data-stu-id="df894-104">SYNTAX</span></span>

### <span data-ttu-id="df894-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="df894-105">ByFactoryName (Default)</span></span>
```
Save-AzDataFactoryLog [-DataFactoryName] <String> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df894-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="df894-106">ByFactoryObject</span></span>
```
Save-AzDataFactoryLog [-DataFactory] <PSDataFactory> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df894-107">說明</span><span class="sxs-lookup"><span data-stu-id="df894-107">DESCRIPTION</span></span>
<span data-ttu-id="df894-108">**AzDataFactoryLog** Cmdlet 會將與 Azure HDInsight 處理的記錄檔案下載到豬或 Hive 專案或自訂活動到您的本機硬碟。</span><span class="sxs-lookup"><span data-stu-id="df894-108">The **Save-AzDataFactoryLog** cmdlet downloads log files associated with Azure HDInsight processing of Pig or Hive projects or for custom activities to your local hard drive.</span></span>
<span data-ttu-id="df894-109">您必須先執行 Get-AzDataFactoryRun Cmdlet，以取得資料切片的活動執行 ID，然後使用該識別碼來從二進位大型物件中檢索記錄檔， (BLOB) 與 HDInsight 群集相關聯的儲存空間。</span><span class="sxs-lookup"><span data-stu-id="df894-109">You first run the Get-AzDataFactoryRun cmdlet to get an ID for an activity run for a data slice, and then use that ID to retrieve log files from the binary large object (BLOB) storage associated with the HDInsight cluster.</span></span>
<span data-ttu-id="df894-110">如果您沒有指定 *DownloadLogs* 參數，則此 Cmdlet 只會傳回記錄檔的位置。</span><span class="sxs-lookup"><span data-stu-id="df894-110">If you do not specify the *DownloadLogs* parameter, the cmdlet just returns the location of log files.</span></span>
<span data-ttu-id="df894-111">如果您指定 *DownloadLogs* 但未指定輸出目錄 ( *輸出* 參數) ，則會將記錄檔案下載到預設的 [檔] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="df894-111">If you specify *DownloadLogs* without specifying an output directory ( *Output* parameter), the log files are downloaded to the default Documents folder.</span></span>
<span data-ttu-id="df894-112">如果您指定 *DownloadLogs* ，並將輸出檔案夾 ( *輸出* ) ，則會將記錄檔案下載到指定的資料夾。</span><span class="sxs-lookup"><span data-stu-id="df894-112">If you specify *DownloadLogs* along with an output folder ( *Output* ), the log files are downloaded to the specified folder.</span></span>

## <span data-ttu-id="df894-113">示例</span><span class="sxs-lookup"><span data-stu-id="df894-113">EXAMPLES</span></span>

### <span data-ttu-id="df894-114">範例1：將記錄檔儲存至特定資料夾</span><span class="sxs-lookup"><span data-stu-id="df894-114">Example 1: Save log files to a specific folder</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs -Output "C:\Test"
```

<span data-ttu-id="df894-115">這個命令會將活動執行的記錄檔儲存在名為841b77c9-d56c-48d1-99a3-8c16c3e77d39 的資料工廠中，其中的活動屬於名為「ADF」的資源群組中名為 LogProcessingFactory 的管線。</span><span class="sxs-lookup"><span data-stu-id="df894-115">This command saves log files for the activity run with the ID of 841b77c9-d56c-48d1-99a3-8c16c3e77d39 where the activity belongs to a pipeline in the data factory named LogProcessingFactory in the resource group named ADF.</span></span>
<span data-ttu-id="df894-116">記錄檔會儲存到 [C:\Test] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="df894-116">The log files are saved to the C:\Test folder.</span></span>

### <span data-ttu-id="df894-117">範例2：將記錄檔儲存至預設的檔資料夾</span><span class="sxs-lookup"><span data-stu-id="df894-117">Example 2: Save log files to default Documents folder</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs
```

<span data-ttu-id="df894-118">這個命令會將記錄檔案儲存到 [檔] 資料夾 (預設) 。</span><span class="sxs-lookup"><span data-stu-id="df894-118">This command saves log files to Documents folder (default).</span></span>

### <span data-ttu-id="df894-119">範例3：取得記錄檔的位置</span><span class="sxs-lookup"><span data-stu-id="df894-119">Example 3: Get the location of log files</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39"
```

<span data-ttu-id="df894-120">這個命令會傳回記錄檔的位置。</span><span class="sxs-lookup"><span data-stu-id="df894-120">This command returns the location of log files.</span></span>
<span data-ttu-id="df894-121">請注意，未指定 *DownloadLogs* 。</span><span class="sxs-lookup"><span data-stu-id="df894-121">Note that *DownloadLogs* is not specified.</span></span>

## <span data-ttu-id="df894-122">參數</span><span class="sxs-lookup"><span data-stu-id="df894-122">PARAMETERS</span></span>

### <span data-ttu-id="df894-123">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="df894-123">-DataFactory</span></span>
<span data-ttu-id="df894-124">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="df894-124">Specifies a **PSDataFactory** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df894-125">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="df894-125">-DataFactoryName</span></span>
<span data-ttu-id="df894-126">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="df894-126">Specifies the name of a data factory.</span></span>
<span data-ttu-id="df894-127">這個 Cmdlet 會下載此參數指定之資料工廠的記錄檔案。</span><span class="sxs-lookup"><span data-stu-id="df894-127">This cmdlet downloads log files for the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df894-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df894-128">-DefaultProfile</span></span>
<span data-ttu-id="df894-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="df894-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df894-130">-DownloadLogs</span><span class="sxs-lookup"><span data-stu-id="df894-130">-DownloadLogs</span></span>
<span data-ttu-id="df894-131">表示此 Cmdlet 會將記錄檔案下載到您的本機電腦。</span><span class="sxs-lookup"><span data-stu-id="df894-131">Indicates that this cmdlet downloads log files to your local computer.</span></span>
<span data-ttu-id="df894-132">如果未指定 *Ouptut* 資料夾，檔案會儲存至子資料夾底下的 [檔] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="df894-132">If *Ouptut* folder is not specified, files are saved to Documents folder under a subfolder.</span></span>

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

### <span data-ttu-id="df894-133">-識別碼</span><span class="sxs-lookup"><span data-stu-id="df894-133">-Id</span></span>
<span data-ttu-id="df894-134">指定資料切片的活動執行 ID。</span><span class="sxs-lookup"><span data-stu-id="df894-134">Specifies the ID of the activity run for the data slice.</span></span>
<span data-ttu-id="df894-135">使用 Get-AzDataFactoryRun Cmdlet 來取得 ID。</span><span class="sxs-lookup"><span data-stu-id="df894-135">Use the Get-AzDataFactoryRun cmdlet to get an ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df894-136">-輸出</span><span class="sxs-lookup"><span data-stu-id="df894-136">-Output</span></span>
<span data-ttu-id="df894-137">指定儲存下載的記錄檔的輸出檔案夾。</span><span class="sxs-lookup"><span data-stu-id="df894-137">Specifies the output folder in which the downloaded log files are saved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df894-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df894-138">-ResourceGroupName</span></span>
<span data-ttu-id="df894-139">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="df894-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="df894-140">這個 Cmdlet 會建立屬於此參數指定之群組的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="df894-140">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df894-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df894-141">CommonParameters</span></span>
<span data-ttu-id="df894-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="df894-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df894-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="df894-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df894-144">輸入</span><span class="sxs-lookup"><span data-stu-id="df894-144">INPUTS</span></span>

### <span data-ttu-id="df894-145">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="df894-145">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="df894-146">System.object</span><span class="sxs-lookup"><span data-stu-id="df894-146">System.String</span></span>

## <span data-ttu-id="df894-147">輸出</span><span class="sxs-lookup"><span data-stu-id="df894-147">OUTPUTS</span></span>

### <span data-ttu-id="df894-148">PSRunLogInfo 中的 DataFactories。</span><span class="sxs-lookup"><span data-stu-id="df894-148">Microsoft.Azure.Commands.DataFactories.Models.PSRunLogInfo</span></span>

## <span data-ttu-id="df894-149">筆記</span><span class="sxs-lookup"><span data-stu-id="df894-149">NOTES</span></span>
* <span data-ttu-id="df894-150">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="df894-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="df894-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="df894-151">RELATED LINKS</span></span>

[<span data-ttu-id="df894-152">AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="df894-152">Get-AzDataFactoryRun</span></span>](./Get-AzDataFactoryRun.md)

[<span data-ttu-id="df894-153">AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="df894-153">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="df894-154">新-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="df894-154">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="df894-155">移除-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="df894-155">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="df894-156">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="df894-156">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="df894-157">暫停-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="df894-157">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


