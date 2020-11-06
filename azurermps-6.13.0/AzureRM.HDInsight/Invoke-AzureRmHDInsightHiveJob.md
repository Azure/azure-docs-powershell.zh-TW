---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 3C6DCC81-82F7-4044-AFBC-4EE1BCC306F2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/invoke-azurermhdinsighthivejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Invoke-AzureRmHDInsightHiveJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Invoke-AzureRmHDInsightHiveJob.md
ms.openlocfilehash: 36def3904621991bee4d3f0f8ad5d3590a4c097b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449147"
---
# <span data-ttu-id="73cd4-101">Invoke-AzureRmHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="73cd4-101">Invoke-AzureRmHDInsightHiveJob</span></span>

## <span data-ttu-id="73cd4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="73cd4-102">SYNOPSIS</span></span>
<span data-ttu-id="73cd4-103">將 Hive 查詢提交至 HDInsight 群集，並以一個作業來檢索查詢結果。</span><span class="sxs-lookup"><span data-stu-id="73cd4-103">Submits a Hive query to an HDInsight cluster and retrieves query results in one operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73cd4-104">句法</span><span class="sxs-lookup"><span data-stu-id="73cd4-104">SYNTAX</span></span>

```
Invoke-AzureRmHDInsightHiveJob [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultContainer <String>] [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73cd4-105">說明</span><span class="sxs-lookup"><span data-stu-id="73cd4-105">DESCRIPTION</span></span>
<span data-ttu-id="73cd4-106">**AzureRmHDInsightHiveJob** Cmdlet 會將 Hive 查詢提交至 Azure HDInsight 群集，並在一個操作中檢索查詢結果。</span><span class="sxs-lookup"><span data-stu-id="73cd4-106">The **Invoke-AzureRmHDInsightHiveJob** cmdlet submits a Hive query to an Azure HDInsight cluster and retrieves query results in one operation.</span></span>
<span data-ttu-id="73cd4-107">在呼叫 **AzureRmHDInsightHiveJob** 前，請先使用 Use-AzureRmHDInsightCluster Cmdlet，以指定將用於查詢的群集。</span><span class="sxs-lookup"><span data-stu-id="73cd4-107">Use the Use-AzureRmHDInsightCluster cmdlet before calling **Invoke-AzureRmHDInsightHiveJob** to specify which cluster will be used for the query.</span></span>

## <span data-ttu-id="73cd4-108">示例</span><span class="sxs-lookup"><span data-stu-id="73cd4-108">EXAMPLES</span></span>

### <span data-ttu-id="73cd4-109">範例1：將 Hive 查詢提交至 Azure HDInsight 群集</span><span class="sxs-lookup"><span data-stu-id="73cd4-109">Example 1: Submit a Hive query to an Azure HDInsight cluster</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> Use-AzureRmHDInsightCluster `
            -ClusterCredential $clusterCreds `
            -ClusterName $clusterName

PS C:\> Invoke-AzureRmHDInsightHiveJob -StatusFolder $statusFolder `
            -Query $query `
            -DefaultContainer $storageAccountContainer `
            -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
            -DefaultStorageAccountKey $storageAccountKey
```

<span data-ttu-id="73cd4-110">這個命令會將查詢顯示表格提交到名為 [您的-hadoop-001] 的群集。</span><span class="sxs-lookup"><span data-stu-id="73cd4-110">This command submits the query SHOW TABLES to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="73cd4-111">參數</span><span class="sxs-lookup"><span data-stu-id="73cd4-111">PARAMETERS</span></span>

### <span data-ttu-id="73cd4-112">-引數</span><span class="sxs-lookup"><span data-stu-id="73cd4-112">-Arguments</span></span>
<span data-ttu-id="73cd4-113">指定作業的引數陣列。</span><span class="sxs-lookup"><span data-stu-id="73cd4-113">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="73cd4-114">引數會以命令列引數的形式傳遞給每個任務。</span><span class="sxs-lookup"><span data-stu-id="73cd4-114">The arguments are passed as command-line arguments to each task.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73cd4-115">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="73cd4-115">-DefaultContainer</span></span>
<span data-ttu-id="73cd4-116">指定 HDInsight 群集使用的預設 Azure 儲存空間帳戶中預設容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="73cd4-116">Specifies the name of the default container in the default Azure Storage account that an HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="73cd4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73cd4-117">-DefaultProfile</span></span>
<span data-ttu-id="73cd4-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="73cd4-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73cd4-119">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="73cd4-119">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="73cd4-120">指定 HDInsight 群集使用之預設儲存空間帳戶的帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="73cd4-120">Specifies the account key for the default storage account that the HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="73cd4-121">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="73cd4-121">-DefaultStorageAccountName</span></span>
<span data-ttu-id="73cd4-122">指定 HDInsight 群集使用的預設儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="73cd4-122">Specifies the name of the default storage account that the HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="73cd4-123">-定義</span><span class="sxs-lookup"><span data-stu-id="73cd4-123">-Defines</span></span>
<span data-ttu-id="73cd4-124">指定要在作業執行時設定的 Hadoop 配置值。</span><span class="sxs-lookup"><span data-stu-id="73cd4-124">Specifies Hadoop configuration values to set when a job runs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73cd4-125">檔案</span><span class="sxs-lookup"><span data-stu-id="73cd4-125">-File</span></span>
<span data-ttu-id="73cd4-126">指定包含要執行查詢的 Azure 儲存體中檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="73cd4-126">Specifies the path to a file in Azure Storage that contains the query to run.</span></span>
<span data-ttu-id="73cd4-127">您可以使用這個參數，而不是 *Query* 參數。</span><span class="sxs-lookup"><span data-stu-id="73cd4-127">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="73cd4-128">-檔案</span><span class="sxs-lookup"><span data-stu-id="73cd4-128">-Files</span></span>
<span data-ttu-id="73cd4-129">指定 Hive 作業所需的檔案集合。</span><span class="sxs-lookup"><span data-stu-id="73cd4-129">Specifies a collection of files that are required for a Hive job.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73cd4-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="73cd4-130">-JobName</span></span>
<span data-ttu-id="73cd4-131">指定 Hive 工作的名稱。</span><span class="sxs-lookup"><span data-stu-id="73cd4-131">Specifies the name of a Hive job.</span></span>
<span data-ttu-id="73cd4-132">如果您沒有指定此參數，這個 Cmdlet 會使用預設值：「Hive：」 \<first 100 characters of Query\> 。</span><span class="sxs-lookup"><span data-stu-id="73cd4-132">If you do not specify this parameter, this cmdlet uses the default value: "Hive: \<first 100 characters of Query\>".</span></span>

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

### <span data-ttu-id="73cd4-133">-Query</span><span class="sxs-lookup"><span data-stu-id="73cd4-133">-Query</span></span>
<span data-ttu-id="73cd4-134">指定 Hive 查詢。</span><span class="sxs-lookup"><span data-stu-id="73cd4-134">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="73cd4-135">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="73cd4-135">-RunAsFileJob</span></span>
<span data-ttu-id="73cd4-136">指示這個 Cmdlet 會在預設的 Azure 儲存空間帳戶中建立檔案，以儲存查詢。</span><span class="sxs-lookup"><span data-stu-id="73cd4-136">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="73cd4-137">這個 Cmdlet 會提交參照此檔案做為腳本以執行的工作。</span><span class="sxs-lookup"><span data-stu-id="73cd4-137">This cmdlet submits the job that references this file as a script to run.</span></span>
<span data-ttu-id="73cd4-138">您可以使用這個功能來處理特殊的字元，例如百分號 (% ) ，這些字元會在透過 Templeton 提交作業時失敗，因為 Templeton 會使用百分號符號作為 URL 參數來轉譯查詢。</span><span class="sxs-lookup"><span data-stu-id="73cd4-138">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="73cd4-139">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="73cd4-139">-StatusFolder</span></span>
<span data-ttu-id="73cd4-140">指定包含工作之標準輸出和錯誤輸出的資料夾位置。</span><span class="sxs-lookup"><span data-stu-id="73cd4-140">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="73cd4-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73cd4-141">CommonParameters</span></span>
<span data-ttu-id="73cd4-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="73cd4-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73cd4-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="73cd4-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73cd4-144">輸入</span><span class="sxs-lookup"><span data-stu-id="73cd4-144">INPUTS</span></span>

### <span data-ttu-id="73cd4-145">所有</span><span class="sxs-lookup"><span data-stu-id="73cd4-145">None</span></span>

## <span data-ttu-id="73cd4-146">輸出</span><span class="sxs-lookup"><span data-stu-id="73cd4-146">OUTPUTS</span></span>

### <span data-ttu-id="73cd4-147">System.object</span><span class="sxs-lookup"><span data-stu-id="73cd4-147">System.String</span></span>

## <span data-ttu-id="73cd4-148">筆記</span><span class="sxs-lookup"><span data-stu-id="73cd4-148">NOTES</span></span>

## <span data-ttu-id="73cd4-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="73cd4-149">RELATED LINKS</span></span>

[<span data-ttu-id="73cd4-150">使用-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="73cd4-150">Use-AzureRmHDInsightCluster</span></span>](./Use-AzureRmHDInsightCluster.md)


