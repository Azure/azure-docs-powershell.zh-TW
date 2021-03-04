---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 4C3CF283-DD4F-4D2A-ABEC-84AC7B005D6A
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/add-azhdinsightconfigvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
ms.openlocfilehash: d5179bd15212e2d5bfa7eb5d903b2c37620ffb23
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911673"
---
# <span data-ttu-id="bc18b-101">Add-AzHDInsightConfigValue</span><span class="sxs-lookup"><span data-stu-id="bc18b-101">Add-AzHDInsightConfigValue</span></span>

## <span data-ttu-id="bc18b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bc18b-102">SYNOPSIS</span></span>
<span data-ttu-id="bc18b-103">新增 Hadoop 組配置值自訂和/或 Hive 共用文件庫自訂至組組物件。</span><span class="sxs-lookup"><span data-stu-id="bc18b-103">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

## <span data-ttu-id="bc18b-104">語法</span><span class="sxs-lookup"><span data-stu-id="bc18b-104">SYNTAX</span></span>

```
Add-AzHDInsightConfigValue [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-SparkDefaults <Hashtable>] [-SparkThriftConf <Hashtable>] [-Spark2Defaults <Hashtable>]
 [-Spark2ThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc18b-105">描述</span><span class="sxs-lookup"><span data-stu-id="bc18b-105">DESCRIPTION</span></span>
<span data-ttu-id="bc18b-106">**Add-AzHDInsightConfigValue** Cmdlet 會新增 Hadoop 組配置值自訂，例如 core-site.xml 或 hive-site.xml，以及/或 Hive 共用文件庫自訂至由 New-AzHDInsightClusterConfig Cmdlet 所建立 HDInsight 組式物件。</span><span class="sxs-lookup"><span data-stu-id="bc18b-106">The **Add-AzHDInsightConfigValue** cmdlet adds a Hadoop configuration value customization, such as core-site.xml or hive-site.xml, and/or a Hive shared library customization to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="bc18b-107">例子</span><span class="sxs-lookup"><span data-stu-id="bc18b-107">EXAMPLES</span></span>

### <span data-ttu-id="bc18b-108">範例 1：在組物件中新增自訂群組組值</span><span class="sxs-lookup"><span data-stu-id="bc18b-108">Example 1: Add a custom configuration value to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value

PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Config values
PS C:\> $coreConfigs = @{"io.file.buffer.size"="300000"}
PS C:\> $mapRedConfigs = @{"mapred.map.max.attempts"="2"}

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightConfigValue `
                -Core $coreConfigs `
                -MapRed $mapRedConfigs `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageAccountContainer
```

<span data-ttu-id="bc18b-109">此命令會將 Hadoop 組組值新增到名為 your-hadoop-001 的組錦。</span><span class="sxs-lookup"><span data-stu-id="bc18b-109">This command adds a Hadoop configuration value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="bc18b-110">參數</span><span class="sxs-lookup"><span data-stu-id="bc18b-110">PARAMETERS</span></span>

### <span data-ttu-id="bc18b-111">-Config</span><span class="sxs-lookup"><span data-stu-id="bc18b-111">-Config</span></span>
<span data-ttu-id="bc18b-112">指定此 Cmdlet 修改的 HDInsight 集區組物件。</span><span class="sxs-lookup"><span data-stu-id="bc18b-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="bc18b-113">此物件是由 Cmdlet New-AzHDInsightClusterConfig建立。</span><span class="sxs-lookup"><span data-stu-id="bc18b-113">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc18b-114">-Core</span><span class="sxs-lookup"><span data-stu-id="bc18b-114">-Core</span></span>
<span data-ttu-id="bc18b-115">指定此 HDInsight 組組的核心網站組式。</span><span class="sxs-lookup"><span data-stu-id="bc18b-115">Specifies the Core Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="bc18b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc18b-116">-DefaultProfile</span></span>
<span data-ttu-id="bc18b-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="bc18b-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bc18b-118">-HBaseEnv</span><span class="sxs-lookup"><span data-stu-id="bc18b-118">-HBaseEnv</span></span>
<span data-ttu-id="bc18b-119">指定此 HDInsight 簇的 HBase Env 組式。</span><span class="sxs-lookup"><span data-stu-id="bc18b-119">Specifies the HBase Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="bc18b-120">-HBaseSite</span><span class="sxs-lookup"><span data-stu-id="bc18b-120">-HBaseSite</span></span>
<span data-ttu-id="bc18b-121">指定此 HDInsight 集的 HBase 網站組式組。</span><span class="sxs-lookup"><span data-stu-id="bc18b-121">Specifies the HBase Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="bc18b-122">-Hdfs</span><span class="sxs-lookup"><span data-stu-id="bc18b-122">-Hdfs</span></span>
<span data-ttu-id="bc18b-123">指定此 HDInsight 集的 HDFS 組式。</span><span class="sxs-lookup"><span data-stu-id="bc18b-123">Specifies the HDFS configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="bc18b-124">-HiveEnv</span><span class="sxs-lookup"><span data-stu-id="bc18b-124">-HiveEnv</span></span>
<span data-ttu-id="bc18b-125">指定此 HDInsight 簇的 Hive Env 組式組。</span><span class="sxs-lookup"><span data-stu-id="bc18b-125">Specifies the Hive Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="bc18b-126">-HiveSite</span><span class="sxs-lookup"><span data-stu-id="bc18b-126">-HiveSite</span></span>
<span data-ttu-id="bc18b-127">指定此 HDInsight 組群的病毒網站組式。</span><span class="sxs-lookup"><span data-stu-id="bc18b-127">Specifies the Hive Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="bc18b-128">-MapRed</span><span class="sxs-lookup"><span data-stu-id="bc18b-128">-MapRed</span></span>
<span data-ttu-id="bc18b-129">指定此 HDInsight 集的 MapRed 網站組式。</span><span class="sxs-lookup"><span data-stu-id="bc18b-129">Specifies the MapRed Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="bc18b-130">-OozieEnv</span><span class="sxs-lookup"><span data-stu-id="bc18b-130">-OozieEnv</span></span>
<span data-ttu-id="bc18b-131">指定此 HDInsight 簇的 Oozie Env 組式組。</span><span class="sxs-lookup"><span data-stu-id="bc18b-131">Specifies the Oozie Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="bc18b-132">-OozieSite</span><span class="sxs-lookup"><span data-stu-id="bc18b-132">-OozieSite</span></span>
<span data-ttu-id="bc18b-133">指定此 HDInsight 集的 Oozie 網站組式。</span><span class="sxs-lookup"><span data-stu-id="bc18b-133">Specifies the Oozie Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="bc18b-134">-RServer</span><span class="sxs-lookup"><span data-stu-id="bc18b-134">-RServer</span></span>
<span data-ttu-id="bc18b-135">指定 RServer 群組原則。</span><span class="sxs-lookup"><span data-stu-id="bc18b-135">Specifies the RServer configurations.</span></span> <span data-ttu-id="bc18b-136">僅適用于 RServer 群。</span><span class="sxs-lookup"><span data-stu-id="bc18b-136">Valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="bc18b-137">-Spark2Defaults</span><span class="sxs-lookup"><span data-stu-id="bc18b-137">-Spark2Defaults</span></span>
<span data-ttu-id="bc18b-138">指定此 HDInsight 簇的 Spark2 預設值組式。</span><span class="sxs-lookup"><span data-stu-id="bc18b-138">Specifies the Spark2 Defaults configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="bc18b-139">-Spark2ThriftConf</span><span class="sxs-lookup"><span data-stu-id="bc18b-139">-Spark2ThriftConf</span></span>
<span data-ttu-id="bc18b-140">指定此 HDInsight 簇的 Spark2 Thrift SparkConf 組式。</span><span class="sxs-lookup"><span data-stu-id="bc18b-140">Specifies the Spark2 Thrift SparkConf configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="bc18b-141">-SparkDefaults</span><span class="sxs-lookup"><span data-stu-id="bc18b-141">-SparkDefaults</span></span>
<span data-ttu-id="bc18b-142">指定此 HDInsight 簇的 Spark 預設值組式。</span><span class="sxs-lookup"><span data-stu-id="bc18b-142">Specifies the Spark Defaults configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="bc18b-143">-SparkThriftConf</span><span class="sxs-lookup"><span data-stu-id="bc18b-143">-SparkThriftConf</span></span>
<span data-ttu-id="bc18b-144">指定此 HDInsight 簇的 Spark Thrift SparkConf 組式。</span><span class="sxs-lookup"><span data-stu-id="bc18b-144">Specifies the Spark Thrift SparkConf configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="bc18b-145">-風雪</span><span class="sxs-lookup"><span data-stu-id="bc18b-145">-Storm</span></span>
<span data-ttu-id="bc18b-146">指定此 HDInsight 集區之暴風網站組式。</span><span class="sxs-lookup"><span data-stu-id="bc18b-146">Specifies the Storm Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="bc18b-147">-Tez</span><span class="sxs-lookup"><span data-stu-id="bc18b-147">-Tez</span></span>
<span data-ttu-id="bc18b-148">指定此 HDInsight 集的 Tez 網站組式組。</span><span class="sxs-lookup"><span data-stu-id="bc18b-148">Specifies the Tez Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="bc18b-149">-WebHCat</span><span class="sxs-lookup"><span data-stu-id="bc18b-149">-WebHCat</span></span>
<span data-ttu-id="bc18b-150">指定此 HDInsight 集的 WebHCat 網站組式。</span><span class="sxs-lookup"><span data-stu-id="bc18b-150">Specifies the WebHCat Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="bc18b-151">-一線</span><span class="sxs-lookup"><span data-stu-id="bc18b-151">-Yarn</span></span>
<span data-ttu-id="bc18b-152">指定此 HDInsight 組群的一組使用時，使用一組 100 分的 201004</a1>。</a2></span><span class="sxs-lookup"><span data-stu-id="bc18b-152">Specifies the YARN Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="bc18b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc18b-153">CommonParameters</span></span>
<span data-ttu-id="bc18b-154">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bc18b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc18b-155">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bc18b-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc18b-156">輸入</span><span class="sxs-lookup"><span data-stu-id="bc18b-156">INPUTS</span></span>

### <span data-ttu-id="bc18b-157">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="bc18b-157">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="bc18b-158">輸出</span><span class="sxs-lookup"><span data-stu-id="bc18b-158">OUTPUTS</span></span>

### <span data-ttu-id="bc18b-159">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="bc18b-159">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="bc18b-160">筆記</span><span class="sxs-lookup"><span data-stu-id="bc18b-160">NOTES</span></span>

## <span data-ttu-id="bc18b-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="bc18b-161">RELATED LINKS</span></span>

[<span data-ttu-id="bc18b-162">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="bc18b-162">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


