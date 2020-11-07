---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 6F89C297-4D3D-4DAD-A63A-FCC51A86BF43
online version: ''
schema: 2.0.0
ms.openlocfilehash: 542b2fb83b69fe5eb63ac6b8b979df6cc8051ed2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967174"
---
# <span data-ttu-id="7650b-101">Add-AzureHDInsightConfigValues</span><span class="sxs-lookup"><span data-stu-id="7650b-101">Add-AzureHDInsightConfigValues</span></span>

## <span data-ttu-id="7650b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7650b-102">SYNOPSIS</span></span>
<span data-ttu-id="7650b-103">將 Hadoop 設定值自訂或蜂巢共用文件庫自訂新增至 HDInsight 群集設定。</span><span class="sxs-lookup"><span data-stu-id="7650b-103">Adds a Hadoop configuration value customization or a Hive shared library customization to an HDInsight cluster configuration.</span></span>

## <span data-ttu-id="7650b-104">句法</span><span class="sxs-lookup"><span data-stu-id="7650b-104">SYNTAX</span></span>

```
Add-AzureHDInsightConfigValues -Config <AzureHDInsightConfig> [-Core <Hashtable>] [-Yarn <Hashtable>]
 [-Hdfs <Hashtable>] [-Hive <AzureHDInsightHiveConfiguration>]
 [-MapReduce <AzureHDInsightMapReduceConfiguration>] [-Oozie <AzureHDInsightOozieConfiguration>]
 [-Storm <Hashtable>] [-Spark <Hashtable>] [-HBase <AzureHDInsightHBaseConfiguration>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7650b-105">說明</span><span class="sxs-lookup"><span data-stu-id="7650b-105">DESCRIPTION</span></span>
<span data-ttu-id="7650b-106">此版本的 Azure PowerShell HDInsight 已被否決。</span><span class="sxs-lookup"><span data-stu-id="7650b-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="7650b-107">這些 Cmdlet 將會在2017年1月1日移除。</span><span class="sxs-lookup"><span data-stu-id="7650b-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="7650b-108">請使用較新版本的 Azure PowerShell HDInsight。</span><span class="sxs-lookup"><span data-stu-id="7650b-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="7650b-109">如需如何使用新的 HDInsight 建立群集的相關資訊，請參閱 [使用 Azure PowerShell 在 HDInsight 中建立以 Linux 為基礎的群集](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/)。</span><span class="sxs-lookup"><span data-stu-id="7650b-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="7650b-110">如需如何使用 Azure PowerShell 和其他方法提交作業的相關資訊，請參閱 [在 HDInsight 中提交 Hadoop 作業](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)。</span><span class="sxs-lookup"><span data-stu-id="7650b-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="7650b-111">如需有關 Azure PowerShell HDInsight 的參考資訊，請參閱 [Azure HDInsight Cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx)。</span><span class="sxs-lookup"><span data-stu-id="7650b-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="7650b-112">**AzureHDInsightConfigValues** Cmdlet 會將 Hadoop 設定值自訂（例如 Core-site.xml 或 Hive-site.xml）或蜂巢共用文件庫自訂新增至 Azure HDInsight 群集設定。</span><span class="sxs-lookup"><span data-stu-id="7650b-112">The **Add-AzureHDInsightConfigValues** cmdlet adds a Hadoop configuration value customization, such as Core-site.xml or Hive-site.xml, or a Hive shared library customization to an Azure HDInsight cluster configuration.</span></span>

<span data-ttu-id="7650b-113">Cmdlet 會將自訂設定值新增到指定的設定物件。</span><span class="sxs-lookup"><span data-stu-id="7650b-113">The cmdlet adds custom configuration values to a specified configuration object.</span></span>
<span data-ttu-id="7650b-114">部署群集時，自訂設定會新增至相關 Hadoop services 的設定檔案中。</span><span class="sxs-lookup"><span data-stu-id="7650b-114">The custom settings are added to the configuration files of the relevant Hadoop services when the cluster is deployed.</span></span>

## <span data-ttu-id="7650b-115">示例</span><span class="sxs-lookup"><span data-stu-id="7650b-115">EXAMPLES</span></span>

### <span data-ttu-id="7650b-116">範例1：設定群集</span><span class="sxs-lookup"><span data-stu-id="7650b-116">Example 1: Configure a cluster</span></span>
```
PS C:\>$HiveConfigValues = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightHiveConfiguration'
PS C:\> $HiveConfigValues.Configuration = @{ hive.exec.compress.output = true }
PS C:\> $HiveConfigValues.AdditionalLibraries = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightDefaultStorageAccount'
PS C:\> $HiveConfigValues.AdditionalLibraries.StorageAccountName = "MyStorageAccount.blob.core.windows.net"
PS C:\> $HiveConfigValues.AdditionalLibraries.StorageAccountKey = (Get-AzureStorageKey -StorageAccountName "MyStorageAccount").Primary
PS C:\> $HiveConfigValues.AdditionalLibraries.StorageContainerName = "MySharedLibContainer"
PS C:\> $OozieConfigValues = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightOozieConfiguration'
PS C:\> $OozieConfigValues.Configuration = @{ hive.exec.compress.output = true }
PS C:\> $MapredConfigValues = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightMapReduceConfiguration'
PS C:\> $MapredConfigValues.Configuration = @{ mapred.map.max.attempts = 2 }
PS C:\> $MapredConfigValues.CapacitySchedulerConfiguration = @{ mapred.capacity-scheduler.init-poll-interval = 1000 }
PS C:\> $Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4
    | Set-AzureHDInsightDefaultStorage -StorageAccountName MyStorageAccount.blob.core.windows.net -StorageAccountKey (Get-AzureStorageKey -StorageAccountName "MyStorageAccount").Primary -StorageContainerName "MyStorageContainer"
    | Add-AzureHDInsightConfigValues -Core @{ io.file.buffer.size = 300000 } -MapReduce $MapredConfigValues -Hive $HiveConfigValues -Oozie $OozieConfigValues
PS C:\> $Config | New-AzureHDInsightCluster -Subscription $SubId -Credential $Creds -Name "MyCluster" -Location "North Europe"
```

<span data-ttu-id="7650b-117">第一個命令會建立新的 **AzureHDInsightHiveConfiguration** 物件，然後將它儲存在 $HiveConfigValues 變數中。</span><span class="sxs-lookup"><span data-stu-id="7650b-117">The first command creates a new **AzureHDInsightHiveConfiguration** object, and then stores it in the $HiveConfigValues variable.</span></span>

<span data-ttu-id="7650b-118">接下來的五個命令會建立 Hive 的配置值，並將這些值儲存為 $HiveConfigValues 的成員。</span><span class="sxs-lookup"><span data-stu-id="7650b-118">The next five commands create configuration values for Hive and store those values as members of $HiveConfigValues.</span></span>

<span data-ttu-id="7650b-119">第七個命令會建立 **AzureHDInsightOozieConfiguration** 物件，然後將它儲存在 $OozieConfigValues 變數中。</span><span class="sxs-lookup"><span data-stu-id="7650b-119">The seventh command creates an **AzureHDInsightOozieConfiguration** object, and then stores it in the $OozieConfigValues variable.</span></span>
<span data-ttu-id="7650b-120">第八個命令會建立 Oozie 的設定值，然後將該值儲存為 $OozieConfigValues 的成員。</span><span class="sxs-lookup"><span data-stu-id="7650b-120">The eighth command creates a configuration value for Oozie, and then stores that values as a member of $OozieConfigValues.</span></span>

<span data-ttu-id="7650b-121">第九個命令會建立 **AzureHDInsightMapReduceConfiguration** 物件，然後將它儲存在 $MapredConfigValues 變數中。</span><span class="sxs-lookup"><span data-stu-id="7650b-121">The ninth command creates an **AzureHDInsightMapReduceConfiguration** object, and then stores it in the $MapredConfigValues variable.</span></span>
<span data-ttu-id="7650b-122">接下來的兩個命令會建立 MapReduce 的配置值，並將這些值儲存為 $MapredConfigValues 的成員。</span><span class="sxs-lookup"><span data-stu-id="7650b-122">The next two commands create configuration values for MapReduce and store those values as members of $MapredConfigValues.</span></span>

<span data-ttu-id="7650b-123">第十二個命令使用 **新的 AzureHDInsightClusterConfig** Cmdlet 來建立 HDInsight 群集設定，然後將它儲存在 $Config 變數中。</span><span class="sxs-lookup"><span data-stu-id="7650b-123">The twelfth command uses the **New-AzureHDInsightClusterConfig** cmdlet to create an HDInsight cluster configuration, and then stores it in the $Config variable.</span></span>
<span data-ttu-id="7650b-124">此命令會使用管線運算子，將 $Config 傳遞給 **AzureHDInsightDefaultStorage** Cmdlet，以更新預設儲存空間設定，以及 **載入 AzureHDInsightConfigValues** Cmdlet，以將新設定值新增到群集設定。</span><span class="sxs-lookup"><span data-stu-id="7650b-124">The command uses the pipeline operator to pass $Config to the **Set-AzureHDInsightDefaultStorage** cmdlet to update the default storage setting and to the **Add-AzureHDInsightConfigValues** cmdlet to add the new configuration values to the cluster configuration.</span></span>

<span data-ttu-id="7650b-125">最後一個命令會使用管線運算子，將 $Config 傳遞到 **新的 AzureHDInsightCluster** Cmdlet，以使用自訂設定來建立新的 HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="7650b-125">The final command uses the pipeline operator to pass $Config to the **New-AzureHDInsightCluster** cmdlet to create a new HDInsight cluster with the customized settings.</span></span>

## <span data-ttu-id="7650b-126">參數</span><span class="sxs-lookup"><span data-stu-id="7650b-126">PARAMETERS</span></span>

### <span data-ttu-id="7650b-127">-Config</span><span class="sxs-lookup"><span data-stu-id="7650b-127">-Config</span></span>
<span data-ttu-id="7650b-128">指定要新增 Hadoop 設定的設定物件。</span><span class="sxs-lookup"><span data-stu-id="7650b-128">Specifies the configuration object to which to add a Hadoop configuration.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7650b-129">核心</span><span class="sxs-lookup"><span data-stu-id="7650b-129">-Core</span></span>
<span data-ttu-id="7650b-130">為 Core-site.xml 指定一組 Hadoop 設定值。</span><span class="sxs-lookup"><span data-stu-id="7650b-130">Specifies a set of Hadoop configuration values for Core-site.xml.</span></span>

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

### <span data-ttu-id="7650b-131">-HBase</span><span class="sxs-lookup"><span data-stu-id="7650b-131">-HBase</span></span>
<span data-ttu-id="7650b-132">為 Hbase-site.xml 指定一組 HBase 設定值。</span><span class="sxs-lookup"><span data-stu-id="7650b-132">Specifies a set of HBase configuration values for Hbase-site.xml.</span></span>

```yaml
Type: AzureHDInsightHBaseConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7650b-133">-Hdfs</span><span class="sxs-lookup"><span data-stu-id="7650b-133">-Hdfs</span></span>
<span data-ttu-id="7650b-134">為 Hdfs-site.xml 指定一組 Hadoop 設定值。</span><span class="sxs-lookup"><span data-stu-id="7650b-134">Specifies a set of Hadoop configuration values for Hdfs-site.xml.</span></span>

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

### <span data-ttu-id="7650b-135">-Hive</span><span class="sxs-lookup"><span data-stu-id="7650b-135">-Hive</span></span>
<span data-ttu-id="7650b-136">指定 Hadoop Hive 服務的自訂物件，包括 Hive-site.xml 與 Hive 共用文件庫的一組 Hadoop 設定值。</span><span class="sxs-lookup"><span data-stu-id="7650b-136">Specifies a customization object for Hadoop Hive service, including a set of Hadoop configuration values for Hive-site.xml and Hive shared libraries.</span></span>

```yaml
Type: AzureHDInsightHiveConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7650b-137">-MapReduce</span><span class="sxs-lookup"><span data-stu-id="7650b-137">-MapReduce</span></span>
<span data-ttu-id="7650b-138">指定 MapReduce 和容量排程的自訂物件。</span><span class="sxs-lookup"><span data-stu-id="7650b-138">Specifies a customization object for MapReduce and the capacity scheduler.</span></span>

```yaml
Type: AzureHDInsightMapReduceConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7650b-139">-Oozie</span><span class="sxs-lookup"><span data-stu-id="7650b-139">-Oozie</span></span>
<span data-ttu-id="7650b-140">指定 Hadoop Oozie service 的自訂物件，包括一組 Oozie-site.xml 的 Hadoop 設定值。</span><span class="sxs-lookup"><span data-stu-id="7650b-140">Specifies a customization object for Hadoop Oozie service, including a set of Hadoop configuration values for Oozie-site.xml.</span></span>

```yaml
Type: AzureHDInsightOozieConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7650b-141">-設定檔</span><span class="sxs-lookup"><span data-stu-id="7650b-141">-Profile</span></span>
<span data-ttu-id="7650b-142">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="7650b-142">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7650b-143">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="7650b-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7650b-144">-Spark</span><span class="sxs-lookup"><span data-stu-id="7650b-144">-Spark</span></span>
<span data-ttu-id="7650b-145">指定 Apache Spark 的自訂物件。</span><span class="sxs-lookup"><span data-stu-id="7650b-145">Specifies a customization object for Apache Spark.</span></span>

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

### <span data-ttu-id="7650b-146">-風暴</span><span class="sxs-lookup"><span data-stu-id="7650b-146">-Storm</span></span>
<span data-ttu-id="7650b-147">指定 Apache 風暴的自訂物件。</span><span class="sxs-lookup"><span data-stu-id="7650b-147">Specifies a customization object for Apache Storm.</span></span>

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

### <span data-ttu-id="7650b-148">-Yarn</span><span class="sxs-lookup"><span data-stu-id="7650b-148">-Yarn</span></span>
<span data-ttu-id="7650b-149">指定 Hadoop YARN 的自訂物件，為 Yarn-site.xml 指定一組自訂的 YARN 設定值。</span><span class="sxs-lookup"><span data-stu-id="7650b-149">Specifies a customization object for Hadoop YARN, specifying a set of customized YARN configuration values for Yarn-site.xml.</span></span>

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

### <span data-ttu-id="7650b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7650b-150">CommonParameters</span></span>
<span data-ttu-id="7650b-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7650b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7650b-152">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7650b-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7650b-153">輸入</span><span class="sxs-lookup"><span data-stu-id="7650b-153">INPUTS</span></span>

## <span data-ttu-id="7650b-154">輸出</span><span class="sxs-lookup"><span data-stu-id="7650b-154">OUTPUTS</span></span>

## <span data-ttu-id="7650b-155">筆記</span><span class="sxs-lookup"><span data-stu-id="7650b-155">NOTES</span></span>

## <span data-ttu-id="7650b-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="7650b-156">RELATED LINKS</span></span>

[<span data-ttu-id="7650b-157">新-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="7650b-157">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="7650b-158">新-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="7650b-158">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)

[<span data-ttu-id="7650b-159">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="7650b-159">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)
