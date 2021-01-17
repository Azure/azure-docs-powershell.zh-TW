---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8BD3B8BD-DC87-4A94-9FCA-611D11D5E065
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightmetastore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightMetastore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightMetastore.md
ms.openlocfilehash: 8102a9ce8ef1117822426d6896edf95d21c46607
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98438335"
---
# <span data-ttu-id="8dd2b-101">Add-AzHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="8dd2b-101">Add-AzHDInsightMetastore</span></span>

## <span data-ttu-id="8dd2b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8dd2b-102">SYNOPSIS</span></span>
<span data-ttu-id="8dd2b-103">新增 SQL 資料庫，以作為 Hive 或 Oozie metastore 至群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="8dd2b-103">Adds a SQL Database to serve as a Hive or Oozie metastore to a cluster configuration object.</span></span>

## <span data-ttu-id="8dd2b-104">句法</span><span class="sxs-lookup"><span data-stu-id="8dd2b-104">SYNTAX</span></span>

```
Add-AzHDInsightMetastore [-Config] <AzureHDInsightConfig> [-MetastoreType] <AzureHDInsightMetastoreType>
 [-SqlAzureServerName] <String> [-DatabaseName] <String> [-Credential] <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8dd2b-105">說明</span><span class="sxs-lookup"><span data-stu-id="8dd2b-105">DESCRIPTION</span></span>
<span data-ttu-id="8dd2b-106">**AzHDInsightMetastore** Cmdlet 會將 Hive 或 Oozie metastore 新增至 New-AzHDInsightClusterConfig Cmdlet 建立的 HDInsight 設定物件。</span><span class="sxs-lookup"><span data-stu-id="8dd2b-106">The **Add-AzHDInsightMetastore** cmdlet adds a Hive or Oozie metastore to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>
<span data-ttu-id="8dd2b-107">Metastore 是 SQL 資料庫，可用於儲存 Hive、Oozie 或兩者的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="8dd2b-107">A metastore is a SQL Database that can used to store metadata for Hive, Oozie, or both.</span></span>

## <span data-ttu-id="8dd2b-108">示例</span><span class="sxs-lookup"><span data-stu-id="8dd2b-108">EXAMPLES</span></span>

### <span data-ttu-id="8dd2b-109">範例1：新增 SQL 資料庫 metastore 至群集設定物件</span><span class="sxs-lookup"><span data-stu-id="8dd2b-109">Example 1: Add a SQL database metastore to the cluster configuration object</span></span>
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

# Hive metastore info
PS C:\> $hiveSqlServer = "your-sqlserver-001"
PS C:\> $hiveDb = "your-sqldb-001"
PS C:\> $hiveCreds = Get-Credential

# Oozie metastore info
PS C:\> $oozieSqlServer = "your-sqlserver-001"
PS C:\> $oozieDb = "your-sqldb-002"
PS C:\> $oozieCreds = Get-Credential

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig  `
            | Add-AzHDInsightMetastore `
                -SqlAzureServerName "$oozieSqlServer.database.contoso.net" `
                -DatabaseName $oozieDb `
                -Credential $oozieCreds `
                -MetastoreType OozieMetastore `
            | Add-AzHDInsightMetastore `
                -SqlAzureServerName "$hiveSqlServer.database.contoso.net" `
                -DatabaseName $hiveDb `
                -Credential $hiveCreds `
                -MetastoreType HiveMetastore `
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
                -StorageContainer $storageContainer
```

<span data-ttu-id="8dd2b-110">這個命令會將 SQL 資料庫 metastore 新增到名為 [您的 hadoop-001] 的群集中。</span><span class="sxs-lookup"><span data-stu-id="8dd2b-110">This command adds a SQL database metastore to the cluster named your-hadoop-001.</span></span>

### <span data-ttu-id="8dd2b-111">範例2：將自訂 Ambari 資料庫新增至群集設定物件</span><span class="sxs-lookup"><span data-stu-id="8dd2b-111">Example 2: Add a custom Ambari database to the cluster configuration object</span></span>
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
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Custom Amari database info
PS C:\> $ambariSqlServer = "your-sqlserver-001"
PS C:\> $ambariDb = "your-sqldb-003"
PS C:\> $ambariCreds = Get-Credential

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig  `
            | Add-AzHDInsightMetastore `
                -SqlAzureServerName "$ambariSqlServer.database.contoso.net" `
                -DatabaseName $ambariDb `
                -Credential $ambariCreds `
                -MetastoreType AmbariDatabase `
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
                -StorageContainer $storageContainer
```

<span data-ttu-id="8dd2b-112">這個命令會將自訂 Ambari 資料庫新增到名為 [hadoop-002] 的群集中。</span><span class="sxs-lookup"><span data-stu-id="8dd2b-112">This command adds a custom Ambari database to the cluster named your-hadoop-002.</span></span>

## <span data-ttu-id="8dd2b-113">參數</span><span class="sxs-lookup"><span data-stu-id="8dd2b-113">PARAMETERS</span></span>

### <span data-ttu-id="8dd2b-114">-Config</span><span class="sxs-lookup"><span data-stu-id="8dd2b-114">-Config</span></span>
<span data-ttu-id="8dd2b-115">指定此 Cmdlet 修改的 HDInsight 群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="8dd2b-115">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="8dd2b-116">這個物件是由 **新的-AzHDInsightClusterConfig** Cmdlet 建立的。</span><span class="sxs-lookup"><span data-stu-id="8dd2b-116">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="8dd2b-117">-認證</span><span class="sxs-lookup"><span data-stu-id="8dd2b-117">-Credential</span></span>
<span data-ttu-id="8dd2b-118">指定要用於 AzureSQL 伺服器資料庫的認證。</span><span class="sxs-lookup"><span data-stu-id="8dd2b-118">Specifies the credentials to use for the AzureSQL Server database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dd2b-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8dd2b-119">-DatabaseName</span></span>
<span data-ttu-id="8dd2b-120">指定要用於此 metastore 的 AzureSQL 伺服器實例上的資料庫。</span><span class="sxs-lookup"><span data-stu-id="8dd2b-120">Specifies the database on the AzureSQL Server instance to use for this metastore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dd2b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dd2b-121">-DefaultProfile</span></span>
<span data-ttu-id="8dd2b-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="8dd2b-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8dd2b-123">-MetastoreType</span><span class="sxs-lookup"><span data-stu-id="8dd2b-123">-MetastoreType</span></span>
<span data-ttu-id="8dd2b-124">指定 metastore 的類型。</span><span class="sxs-lookup"><span data-stu-id="8dd2b-124">Specifies the type of metastore.</span></span>
<span data-ttu-id="8dd2b-125">可能的值為 HiveMetastore 或 OozieMetastore。</span><span class="sxs-lookup"><span data-stu-id="8dd2b-125">Possible values are HiveMetastore or OozieMetastore.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastoreType
Parameter Sets: (All)
Aliases:
Accepted values: HiveMetastore, OozieMetastore, AmbariDatabase

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dd2b-126">-SqlAzureServerName</span><span class="sxs-lookup"><span data-stu-id="8dd2b-126">-SqlAzureServerName</span></span>
<span data-ttu-id="8dd2b-127">指定要用於此 metastore 的 AzureSQL 伺服器實例。</span><span class="sxs-lookup"><span data-stu-id="8dd2b-127">Specifies the AzureSQL Server instance to use for this metastore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dd2b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dd2b-128">CommonParameters</span></span>
<span data-ttu-id="8dd2b-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8dd2b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dd2b-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8dd2b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dd2b-131">輸入</span><span class="sxs-lookup"><span data-stu-id="8dd2b-131">INPUTS</span></span>

### <span data-ttu-id="8dd2b-132">AzureHDInsightConfig （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="8dd2b-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="8dd2b-133">輸出</span><span class="sxs-lookup"><span data-stu-id="8dd2b-133">OUTPUTS</span></span>

### <span data-ttu-id="8dd2b-134">AzureHDInsightConfig （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="8dd2b-134">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="8dd2b-135">筆記</span><span class="sxs-lookup"><span data-stu-id="8dd2b-135">NOTES</span></span>

## <span data-ttu-id="8dd2b-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="8dd2b-136">RELATED LINKS</span></span>

[<span data-ttu-id="8dd2b-137">新-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="8dd2b-137">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


