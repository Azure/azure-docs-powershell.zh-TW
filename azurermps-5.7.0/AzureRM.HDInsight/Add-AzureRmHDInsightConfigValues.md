---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 4C3CF283-DD4F-4D2A-ABEC-84AC7B005D6A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/add-azurermhdinsightconfigvalues
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightConfigValues.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightConfigValues.md
ms.openlocfilehash: 75d68b98d93168d69db4d5120dde41ca1a8f8f2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448663"
---
# <span data-ttu-id="8d5e8-101">Add-AzureRmHDInsightConfigValues</span><span class="sxs-lookup"><span data-stu-id="8d5e8-101">Add-AzureRmHDInsightConfigValues</span></span>

## <span data-ttu-id="8d5e8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8d5e8-102">SYNOPSIS</span></span>
<span data-ttu-id="8d5e8-103">將 Hadoop 設定值自訂和/或配置單元共用文件庫自訂新增至群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="8d5e8-103">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d5e8-104">句法</span><span class="sxs-lookup"><span data-stu-id="8d5e8-104">SYNTAX</span></span>

### <span data-ttu-id="8d5e8-105">Spark1</span><span class="sxs-lookup"><span data-stu-id="8d5e8-105">Spark1</span></span>
```
Add-AzureRmHDInsightConfigValues [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-SparkDefaults <Hashtable>] [-SparkThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8d5e8-106">Spark2</span><span class="sxs-lookup"><span data-stu-id="8d5e8-106">Spark2</span></span>
```
Add-AzureRmHDInsightConfigValues [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-Spark2Defaults <Hashtable>] [-Spark2ThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8d5e8-107">說明</span><span class="sxs-lookup"><span data-stu-id="8d5e8-107">DESCRIPTION</span></span>
<span data-ttu-id="8d5e8-108">**AzureRmHDInsightConfigValues** Cmdlet 會將 Hadoop 設定值自訂（例如 core-site.xml 或 hive-site.xml）及/或配置單元共用文件庫自訂新增至 New-AzureRmHDInsightClusterConfig Cmdlet 建立的 HDInsight 設定物件。</span><span class="sxs-lookup"><span data-stu-id="8d5e8-108">The **Add-AzureRmHDInsightConfigValues** cmdlet adds a Hadoop configuration value customization, such as core-site.xml or hive-site.xml, and/or a Hive shared library customization to the HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="8d5e8-109">示例</span><span class="sxs-lookup"><span data-stu-id="8d5e8-109">EXAMPLES</span></span>

### <span data-ttu-id="8d5e8-110">範例1：將自訂設定值新增至 [群集設定] 物件</span><span class="sxs-lookup"><span data-stu-id="8d5e8-110">Example 1: Add a custom configuration value to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value

PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

# Config values
PS C:\> $coreConfigs = @{"io.file.buffer.size"="300000"}
PS C:\> $mapRedConfigs = @{"mapred.map.max.attempts"="2"}

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig `
            | Add-AzureRmHDInsightConfigValues `
                -Core $coreConfigs `
                -MapRed $mapRedConfigs `
            | New-AzureRmHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageAccountContainer
```

<span data-ttu-id="8d5e8-111">這個命令會將 Hadoop 設定值新增到名為 [hadoop-001] 的群集中。</span><span class="sxs-lookup"><span data-stu-id="8d5e8-111">This command adds a Hadoop configuration value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="8d5e8-112">參數</span><span class="sxs-lookup"><span data-stu-id="8d5e8-112">PARAMETERS</span></span>

### <span data-ttu-id="8d5e8-113">-Config</span><span class="sxs-lookup"><span data-stu-id="8d5e8-113">-Config</span></span>
<span data-ttu-id="8d5e8-114">指定此 Cmdlet 修改的 HDInsight 群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="8d5e8-114">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="8d5e8-115">這個物件是由 New-AzureRmHDInsightClusterConfig Cmdlet 建立的。</span><span class="sxs-lookup"><span data-stu-id="8d5e8-115">This object is created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d5e8-116">核心</span><span class="sxs-lookup"><span data-stu-id="8d5e8-116">-Core</span></span>
<span data-ttu-id="8d5e8-117">指定此 HDInsight 群集的核心網站設定。</span><span class="sxs-lookup"><span data-stu-id="8d5e8-117">Specifies the Core Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="8d5e8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d5e8-118">-DefaultProfile</span></span>
<span data-ttu-id="8d5e8-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="8d5e8-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8d5e8-120">-HBaseEnv</span><span class="sxs-lookup"><span data-stu-id="8d5e8-120">-HBaseEnv</span></span>
<span data-ttu-id="8d5e8-121">指定此 HDInsight 群集的 HBase 配置。</span><span class="sxs-lookup"><span data-stu-id="8d5e8-121">Specifies the HBase Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="8d5e8-122">-HBaseSite</span><span class="sxs-lookup"><span data-stu-id="8d5e8-122">-HBaseSite</span></span>
<span data-ttu-id="8d5e8-123">指定此 HDInsight 群集的 HBase 網站設定。</span><span class="sxs-lookup"><span data-stu-id="8d5e8-123">Specifies the HBase Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="8d5e8-124">-Hdfs</span><span class="sxs-lookup"><span data-stu-id="8d5e8-124">-Hdfs</span></span>
<span data-ttu-id="8d5e8-125">指定此 HDInsight 群集的 HDFS 設定。</span><span class="sxs-lookup"><span data-stu-id="8d5e8-125">Specifies the HDFS configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="8d5e8-126">-HiveEnv</span><span class="sxs-lookup"><span data-stu-id="8d5e8-126">-HiveEnv</span></span>
<span data-ttu-id="8d5e8-127">指定此 HDInsight 群集的 Hive 配置環境設定。</span><span class="sxs-lookup"><span data-stu-id="8d5e8-127">Specifies the Hive Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="8d5e8-128">-HiveSite</span><span class="sxs-lookup"><span data-stu-id="8d5e8-128">-HiveSite</span></span>
<span data-ttu-id="8d5e8-129">指定此 HDInsight 群集的 Hive 網站設定。</span><span class="sxs-lookup"><span data-stu-id="8d5e8-129">Specifies the Hive Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="8d5e8-130">-MapRed</span><span class="sxs-lookup"><span data-stu-id="8d5e8-130">-MapRed</span></span>
<span data-ttu-id="8d5e8-131">指定此 HDInsight 群集的 MapRed 網站設定。</span><span class="sxs-lookup"><span data-stu-id="8d5e8-131">Specifies the MapRed Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="8d5e8-132">-OozieEnv</span><span class="sxs-lookup"><span data-stu-id="8d5e8-132">-OozieEnv</span></span>
<span data-ttu-id="8d5e8-133">指定此 HDInsight 群集的 Oozie 環境設定。</span><span class="sxs-lookup"><span data-stu-id="8d5e8-133">Specifies the Oozie Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="8d5e8-134">-OozieSite</span><span class="sxs-lookup"><span data-stu-id="8d5e8-134">-OozieSite</span></span>
<span data-ttu-id="8d5e8-135">指定此 HDInsight 群集的 Oozie 網站設定。</span><span class="sxs-lookup"><span data-stu-id="8d5e8-135">Specifies the Oozie Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="8d5e8-136">-RServer</span><span class="sxs-lookup"><span data-stu-id="8d5e8-136">-RServer</span></span>
<span data-ttu-id="8d5e8-137">指定 RServer 設定。</span><span class="sxs-lookup"><span data-stu-id="8d5e8-137">Specifies the RServer configurations.</span></span> <span data-ttu-id="8d5e8-138">僅對 RServer 群集有效。</span><span class="sxs-lookup"><span data-stu-id="8d5e8-138">Valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="8d5e8-139">-Spark2Defaults</span><span class="sxs-lookup"><span data-stu-id="8d5e8-139">-Spark2Defaults</span></span>
<span data-ttu-id="8d5e8-140">指定此 HDInsight 群集的 Spark2 預設設定。</span><span class="sxs-lookup"><span data-stu-id="8d5e8-140">Specifies the Spark2 Defaults configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Spark2
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d5e8-141">-Spark2ThriftConf</span><span class="sxs-lookup"><span data-stu-id="8d5e8-141">-Spark2ThriftConf</span></span>
<span data-ttu-id="8d5e8-142">指定此 HDInsight 群集的 Spark2 Thrift SparkConf 設定。</span><span class="sxs-lookup"><span data-stu-id="8d5e8-142">Specifies the Spark2 Thrift SparkConf configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Spark2
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d5e8-143">-SparkDefaults</span><span class="sxs-lookup"><span data-stu-id="8d5e8-143">-SparkDefaults</span></span>
<span data-ttu-id="8d5e8-144">指定此 HDInsight 群集的 Spark 預設設定。</span><span class="sxs-lookup"><span data-stu-id="8d5e8-144">Specifies the Spark Defaults configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Spark1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d5e8-145">-SparkThriftConf</span><span class="sxs-lookup"><span data-stu-id="8d5e8-145">-SparkThriftConf</span></span>
<span data-ttu-id="8d5e8-146">指定此 HDInsight 群集的 Spark Thrift SparkConf 設定。</span><span class="sxs-lookup"><span data-stu-id="8d5e8-146">Specifies the Spark Thrift SparkConf configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Spark1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d5e8-147">-風暴</span><span class="sxs-lookup"><span data-stu-id="8d5e8-147">-Storm</span></span>
<span data-ttu-id="8d5e8-148">指定此 HDInsight 群集的風暴網站設定。</span><span class="sxs-lookup"><span data-stu-id="8d5e8-148">Specifies the Storm Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="8d5e8-149">-Tez</span><span class="sxs-lookup"><span data-stu-id="8d5e8-149">-Tez</span></span>
<span data-ttu-id="8d5e8-150">指定此 HDInsight 群集的 Tez 網站設定。</span><span class="sxs-lookup"><span data-stu-id="8d5e8-150">Specifies the Tez Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="8d5e8-151">-WebHCat</span><span class="sxs-lookup"><span data-stu-id="8d5e8-151">-WebHCat</span></span>
<span data-ttu-id="8d5e8-152">指定此 HDInsight 群集的 WebHCat 網站設定。</span><span class="sxs-lookup"><span data-stu-id="8d5e8-152">Specifies the WebHCat Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="8d5e8-153">-Yarn</span><span class="sxs-lookup"><span data-stu-id="8d5e8-153">-Yarn</span></span>
<span data-ttu-id="8d5e8-154">指定此 HDInsight 群集的 YARN 網站設定。</span><span class="sxs-lookup"><span data-stu-id="8d5e8-154">Specifies the YARN Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="8d5e8-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d5e8-155">CommonParameters</span></span>
<span data-ttu-id="8d5e8-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8d5e8-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d5e8-157">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8d5e8-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d5e8-158">輸入</span><span class="sxs-lookup"><span data-stu-id="8d5e8-158">INPUTS</span></span>

### <span data-ttu-id="8d5e8-159">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="8d5e8-159">AzureHDInsightConfig</span></span>
<span data-ttu-id="8d5e8-160">形參 "Config" 接受管線中 "AzureHDInsightConfig" 類型的值</span><span class="sxs-lookup"><span data-stu-id="8d5e8-160">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="8d5e8-161">輸出</span><span class="sxs-lookup"><span data-stu-id="8d5e8-161">OUTPUTS</span></span>

### <span data-ttu-id="8d5e8-162">AzureHDInsightConfig （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="8d5e8-162">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="8d5e8-163">筆記</span><span class="sxs-lookup"><span data-stu-id="8d5e8-163">NOTES</span></span>

## <span data-ttu-id="8d5e8-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="8d5e8-164">RELATED LINKS</span></span>

[<span data-ttu-id="8d5e8-165">新-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="8d5e8-165">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)


