---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5490BB24-127E-4C21-B85F-B70D817B659A
online version: https://docs.microsoft.com/powershell/module/az.datafactory/save-azdatafactorylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
ms.openlocfilehash: eb2e3c9acd93e8b20c7bdf6f4ee04ef2910a3cbb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916197"
---
# <span data-ttu-id="17eb9-101">Save-AzDataFactoryLog</span><span class="sxs-lookup"><span data-stu-id="17eb9-101">Save-AzDataFactoryLog</span></span>

## <span data-ttu-id="17eb9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="17eb9-102">SYNOPSIS</span></span>
<span data-ttu-id="17eb9-103">從 Azure HDInsight 處理下載記錄檔。</span><span class="sxs-lookup"><span data-stu-id="17eb9-103">Downloads log files from Azure HDInsight processing.</span></span>

## <span data-ttu-id="17eb9-104">語法</span><span class="sxs-lookup"><span data-stu-id="17eb9-104">SYNTAX</span></span>

### <span data-ttu-id="17eb9-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="17eb9-105">ByFactoryName (Default)</span></span>
```
Save-AzDataFactoryLog [-DataFactoryName] <String> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17eb9-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="17eb9-106">ByFactoryObject</span></span>
```
Save-AzDataFactoryLog [-DataFactory] <PSDataFactory> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17eb9-107">描述</span><span class="sxs-lookup"><span data-stu-id="17eb9-107">DESCRIPTION</span></span>
<span data-ttu-id="17eb9-108">**Save-AzDataFactoryLog** Cmdlet 會下載與 Azure HDInsight 處理小明體或病毒專案相關的記錄檔案，或將自訂活動下載到您的本地硬碟。</span><span class="sxs-lookup"><span data-stu-id="17eb9-108">The **Save-AzDataFactoryLog** cmdlet downloads log files associated with Azure HDInsight processing of Pig or Hive projects or for custom activities to your local hard drive.</span></span>
<span data-ttu-id="17eb9-109">您先執行 Get-AzDataFactoryRun Cmdlet，取得資料區執行之活動的識別碼，然後使用該識別碼從與 HDInsight 集區關聯的二進位大型物件 (BLOB) 儲存空間中，取得記錄檔。</span><span class="sxs-lookup"><span data-stu-id="17eb9-109">You first run the Get-AzDataFactoryRun cmdlet to get an ID for an activity run for a data slice, and then use that ID to retrieve log files from the binary large object (BLOB) storage associated with the HDInsight cluster.</span></span>
<span data-ttu-id="17eb9-110">如果您未指定 *DownloadLogs* 參數，Cmdlet 會直接返回記錄檔的位置。</span><span class="sxs-lookup"><span data-stu-id="17eb9-110">If you do not specify the *DownloadLogs* parameter, the cmdlet just returns the location of log files.</span></span>
<span data-ttu-id="17eb9-111">如果您指定 *DownloadLogs* 而不指定輸出 (*輸出* 參數) ，記錄檔案會下載到預設的檔資料夾。</span><span class="sxs-lookup"><span data-stu-id="17eb9-111">If you specify *DownloadLogs* without specifying an output directory (*Output* parameter), the log files are downloaded to the default Documents folder.</span></span>
<span data-ttu-id="17eb9-112">如果您指定 *DownloadLogs* 以及輸出檔案夾 (*輸出*) ，記錄檔會下載到指定的資料夾。</span><span class="sxs-lookup"><span data-stu-id="17eb9-112">If you specify *DownloadLogs* along with an output folder (*Output*), the log files are downloaded to the specified folder.</span></span>

## <span data-ttu-id="17eb9-113">例子</span><span class="sxs-lookup"><span data-stu-id="17eb9-113">EXAMPLES</span></span>

### <span data-ttu-id="17eb9-114">範例 1：將記錄檔儲存至特定資料夾</span><span class="sxs-lookup"><span data-stu-id="17eb9-114">Example 1: Save log files to a specific folder</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs -Output "C:\Test"
```

<span data-ttu-id="17eb9-115">此命令會針對使用識別碼為 841b77c9-d56c-48d1-99a3-8c16c3e77d39 的活動，其中活動屬於名為 ADF 之資源群組中 LogProcessingFactory 之資料工廠中的管線，因此會記錄記錄檔。</span><span class="sxs-lookup"><span data-stu-id="17eb9-115">This command saves log files for the activity run with the ID of 841b77c9-d56c-48d1-99a3-8c16c3e77d39 where the activity belongs to a pipeline in the data factory named LogProcessingFactory in the resource group named ADF.</span></span>
<span data-ttu-id="17eb9-116">記錄檔案會儲存到 C：\Test 資料夾。</span><span class="sxs-lookup"><span data-stu-id="17eb9-116">The log files are saved to the C:\Test folder.</span></span>

### <span data-ttu-id="17eb9-117">範例 2：將記錄檔案儲存到預設的檔資料夾</span><span class="sxs-lookup"><span data-stu-id="17eb9-117">Example 2: Save log files to default Documents folder</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs
```

<span data-ttu-id="17eb9-118">此命令會將記錄檔 (資料夾) 。</span><span class="sxs-lookup"><span data-stu-id="17eb9-118">This command saves log files to Documents folder (default).</span></span>

### <span data-ttu-id="17eb9-119">範例 3：取得記錄檔的位置</span><span class="sxs-lookup"><span data-stu-id="17eb9-119">Example 3: Get the location of log files</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39"
```

<span data-ttu-id="17eb9-120">此命令會返回記錄檔的位置。</span><span class="sxs-lookup"><span data-stu-id="17eb9-120">This command returns the location of log files.</span></span>
<span data-ttu-id="17eb9-121">請注意，*未指定 DownloadLogs。*</span><span class="sxs-lookup"><span data-stu-id="17eb9-121">Note that *DownloadLogs* is not specified.</span></span>

## <span data-ttu-id="17eb9-122">參數</span><span class="sxs-lookup"><span data-stu-id="17eb9-122">PARAMETERS</span></span>

### <span data-ttu-id="17eb9-123">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="17eb9-123">-DataFactory</span></span>
<span data-ttu-id="17eb9-124">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="17eb9-124">Specifies a **PSDataFactory** object.</span></span>

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

### <span data-ttu-id="17eb9-125">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="17eb9-125">-DataFactoryName</span></span>
<span data-ttu-id="17eb9-126">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="17eb9-126">Specifies the name of a data factory.</span></span>
<span data-ttu-id="17eb9-127">此 Cmdlet 會下載此參數指定之資料工廠的記錄檔案。</span><span class="sxs-lookup"><span data-stu-id="17eb9-127">This cmdlet downloads log files for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="17eb9-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17eb9-128">-DefaultProfile</span></span>
<span data-ttu-id="17eb9-129">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="17eb9-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="17eb9-130">-DownloadLogs</span><span class="sxs-lookup"><span data-stu-id="17eb9-130">-DownloadLogs</span></span>
<span data-ttu-id="17eb9-131">表示此 Cmdlet 會下載記錄檔案至您的本地電腦。</span><span class="sxs-lookup"><span data-stu-id="17eb9-131">Indicates that this cmdlet downloads log files to your local computer.</span></span>
<span data-ttu-id="17eb9-132">如果 *未指定輸出* 資料夾，檔案會儲存至子資料夾下的檔資料夾。</span><span class="sxs-lookup"><span data-stu-id="17eb9-132">If *Output* folder is not specified, files are saved to Documents folder under a subfolder.</span></span>

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

### <span data-ttu-id="17eb9-133">-Id</span><span class="sxs-lookup"><span data-stu-id="17eb9-133">-Id</span></span>
<span data-ttu-id="17eb9-134">指定資料區執行之活動的識別碼。</span><span class="sxs-lookup"><span data-stu-id="17eb9-134">Specifies the ID of the activity run for the data slice.</span></span>
<span data-ttu-id="17eb9-135">使用 Get-AzDataFactoryRun Cmdlet 取得識別碼。</span><span class="sxs-lookup"><span data-stu-id="17eb9-135">Use the Get-AzDataFactoryRun cmdlet to get an ID.</span></span>

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

### <span data-ttu-id="17eb9-136">-輸出</span><span class="sxs-lookup"><span data-stu-id="17eb9-136">-Output</span></span>
<span data-ttu-id="17eb9-137">指定儲存下載記錄檔案的輸出檔案夾。</span><span class="sxs-lookup"><span data-stu-id="17eb9-137">Specifies the output folder in which the downloaded log files are saved.</span></span>

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

### <span data-ttu-id="17eb9-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17eb9-138">-ResourceGroupName</span></span>
<span data-ttu-id="17eb9-139">指定 Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="17eb9-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="17eb9-140">此 Cmdlet 會建立屬於此參數指定之群組的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="17eb9-140">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="17eb9-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17eb9-141">CommonParameters</span></span>
<span data-ttu-id="17eb9-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="17eb9-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17eb9-143">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="17eb9-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17eb9-144">輸入</span><span class="sxs-lookup"><span data-stu-id="17eb9-144">INPUTS</span></span>

### <span data-ttu-id="17eb9-145">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="17eb9-145">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="17eb9-146">System.String</span><span class="sxs-lookup"><span data-stu-id="17eb9-146">System.String</span></span>

## <span data-ttu-id="17eb9-147">輸出</span><span class="sxs-lookup"><span data-stu-id="17eb9-147">OUTPUTS</span></span>

### <span data-ttu-id="17eb9-148">Microsoft.Azure.Commands.DataFactories.models.PSRunLogInfo</span><span class="sxs-lookup"><span data-stu-id="17eb9-148">Microsoft.Azure.Commands.DataFactories.Models.PSRunLogInfo</span></span>

## <span data-ttu-id="17eb9-149">筆記</span><span class="sxs-lookup"><span data-stu-id="17eb9-149">NOTES</span></span>
* <span data-ttu-id="17eb9-150">關鍵字：azure、azurerm、arm、resource、management、manager、data、azure</span><span class="sxs-lookup"><span data-stu-id="17eb9-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="17eb9-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="17eb9-151">RELATED LINKS</span></span>

[<span data-ttu-id="17eb9-152">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="17eb9-152">Get-AzDataFactoryRun</span></span>](./Get-AzDataFactoryRun.md)

[<span data-ttu-id="17eb9-153">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="17eb9-153">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="17eb9-154">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="17eb9-154">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="17eb9-155">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="17eb9-155">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="17eb9-156">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="17eb9-156">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="17eb9-157">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="17eb9-157">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


