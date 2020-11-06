---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 580D3388-4E18-4E67-866F-1FCF5E54AB3A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsighthivejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightHiveJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightHiveJobDefinition.md
ms.openlocfilehash: 3e4748a8bc5e5c04868fb7c2d4179c07ea63c905
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447088"
---
# <span data-ttu-id="cf254-101">New-AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="cf254-101">New-AzureRmHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="cf254-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cf254-102">SYNOPSIS</span></span>
<span data-ttu-id="cf254-103">建立 Hive 工作物件。</span><span class="sxs-lookup"><span data-stu-id="cf254-103">Creates a Hive job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf254-104">句法</span><span class="sxs-lookup"><span data-stu-id="cf254-104">SYNTAX</span></span>

```
New-AzureRmHDInsightHiveJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf254-105">說明</span><span class="sxs-lookup"><span data-stu-id="cf254-105">DESCRIPTION</span></span>
<span data-ttu-id="cf254-106">**新的-AzureRmHDInsightHiveJobDefinition** Cmdlet 會定義用於 Azure HDInsight 群集的 Hive 工作物件。</span><span class="sxs-lookup"><span data-stu-id="cf254-106">The **New-AzureRmHDInsightHiveJobDefinition** cmdlet defines a Hive job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="cf254-107">示例</span><span class="sxs-lookup"><span data-stu-id="cf254-107">EXAMPLES</span></span>

### <span data-ttu-id="cf254-108">範例1：建立蜂巢作業定義</span><span class="sxs-lookup"><span data-stu-id="cf254-108">Example 1: Create a Hive job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Hive job details
PS C:\>$statusFolder = "<status folder>"        
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="cf254-109">這個命令會建立一個蜂巢作業定義。</span><span class="sxs-lookup"><span data-stu-id="cf254-109">This command creates a Hive job definition.</span></span>

## <span data-ttu-id="cf254-110">參數</span><span class="sxs-lookup"><span data-stu-id="cf254-110">PARAMETERS</span></span>

### <span data-ttu-id="cf254-111">-引數</span><span class="sxs-lookup"><span data-stu-id="cf254-111">-Arguments</span></span>
<span data-ttu-id="cf254-112">指定作業的引數陣列。</span><span class="sxs-lookup"><span data-stu-id="cf254-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="cf254-113">引數會以命令列引數的形式傳遞給每個任務。</span><span class="sxs-lookup"><span data-stu-id="cf254-113">The arguments are passed as command-line arguments to each task.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf254-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf254-114">-DefaultProfile</span></span>
<span data-ttu-id="cf254-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="cf254-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf254-116">-定義</span><span class="sxs-lookup"><span data-stu-id="cf254-116">-Defines</span></span>
<span data-ttu-id="cf254-117">指定要在作業執行時設定的 Hadoop 配置值。</span><span class="sxs-lookup"><span data-stu-id="cf254-117">Specifies Hadoop configuration values to set for when the job runs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf254-118">檔案</span><span class="sxs-lookup"><span data-stu-id="cf254-118">-File</span></span>
<span data-ttu-id="cf254-119">指定包含要執行之查詢之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="cf254-119">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="cf254-120">該檔案必須在與群集相關聯的儲存空間帳戶上提供。</span><span class="sxs-lookup"><span data-stu-id="cf254-120">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="cf254-121">您可以使用這個參數，而不是 *Query* 參數。</span><span class="sxs-lookup"><span data-stu-id="cf254-121">You can use this parameter instead of the *Query* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf254-122">-檔案</span><span class="sxs-lookup"><span data-stu-id="cf254-122">-Files</span></span>
<span data-ttu-id="cf254-123">指定與 Hive 作業相關聯的檔案集合。</span><span class="sxs-lookup"><span data-stu-id="cf254-123">Specifies a collection of files that are associated with a Hive job.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf254-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="cf254-124">-JobName</span></span>
<span data-ttu-id="cf254-125">指定作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf254-125">Specifies the name of the job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf254-126">-Query</span><span class="sxs-lookup"><span data-stu-id="cf254-126">-Query</span></span>
<span data-ttu-id="cf254-127">指定 Hive 查詢。</span><span class="sxs-lookup"><span data-stu-id="cf254-127">Specifies the Hive query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf254-128">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="cf254-128">-RunAsFileJob</span></span>
<span data-ttu-id="cf254-129">指示這個 Cmdlet 會在預設的 Azure 儲存空間帳戶中建立檔案，以儲存查詢。</span><span class="sxs-lookup"><span data-stu-id="cf254-129">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="cf254-130">這個 Cmdlet 會提交參照此檔案做為腳本以執行的工作。</span><span class="sxs-lookup"><span data-stu-id="cf254-130">This cmdlet submits the job that references this file as a script to run.</span></span>

<span data-ttu-id="cf254-131">您可以使用這個功能來處理特殊的字元，例如百分號 (% ) ，這些字元會在透過 Templeton 提交作業時失敗，因為 Templeton 會使用百分號符號作為 URL 參數來轉譯查詢。</span><span class="sxs-lookup"><span data-stu-id="cf254-131">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="cf254-132">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="cf254-132">-StatusFolder</span></span>
<span data-ttu-id="cf254-133">指定包含工作之標準輸出和錯誤輸出的資料夾位置。</span><span class="sxs-lookup"><span data-stu-id="cf254-133">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf254-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf254-134">CommonParameters</span></span>
<span data-ttu-id="cf254-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cf254-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf254-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cf254-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf254-137">輸入</span><span class="sxs-lookup"><span data-stu-id="cf254-137">INPUTS</span></span>

### <span data-ttu-id="cf254-138">所有</span><span class="sxs-lookup"><span data-stu-id="cf254-138">None</span></span>
<span data-ttu-id="cf254-139">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="cf254-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cf254-140">輸出</span><span class="sxs-lookup"><span data-stu-id="cf254-140">OUTPUTS</span></span>

### <span data-ttu-id="cf254-141">AzureHDInsightHiveJobDefinition （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="cf254-141">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="cf254-142">筆記</span><span class="sxs-lookup"><span data-stu-id="cf254-142">NOTES</span></span>

## <span data-ttu-id="cf254-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="cf254-143">RELATED LINKS</span></span>

[<span data-ttu-id="cf254-144">開始-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="cf254-144">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


