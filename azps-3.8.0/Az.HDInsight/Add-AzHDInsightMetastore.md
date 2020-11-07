---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8BD3B8BD-DC87-4A94-9FCA-611D11D5E065
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightmetastore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightMetastore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightMetastore.md
ms.openlocfilehash: f8971070851da36fb1bf72aef33085e974ef1fb7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93799265"
---
# <span data-ttu-id="a4b68-101">Add-AzHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="a4b68-101">Add-AzHDInsightMetastore</span></span>

## <span data-ttu-id="a4b68-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a4b68-102">SYNOPSIS</span></span>
<span data-ttu-id="a4b68-103">新增 SQL 資料庫，以作為 Hive 或 Oozie metastore 至群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="a4b68-103">Adds a SQL Database to serve as a Hive or Oozie metastore to a cluster configuration object.</span></span>

## <span data-ttu-id="a4b68-104">句法</span><span class="sxs-lookup"><span data-stu-id="a4b68-104">SYNTAX</span></span>

```
Add-AzHDInsightMetastore [-Config] <AzureHDInsightConfig> [-MetastoreType] <AzureHDInsightMetastoreType>
 [-SqlAzureServerName] <String> [-DatabaseName] <String> [-Credential] <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4b68-105">說明</span><span class="sxs-lookup"><span data-stu-id="a4b68-105">DESCRIPTION</span></span>
<span data-ttu-id="a4b68-106">**AzHDInsightMetastore** Cmdlet 會將 Hive 或 Oozie metastore 新增至 New-AzHDInsightClusterConfig Cmdlet 建立的 HDInsight 設定物件。</span><span class="sxs-lookup"><span data-stu-id="a4b68-106">The **Add-AzHDInsightMetastore** cmdlet adds a Hive or Oozie metastore to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>
<span data-ttu-id="a4b68-107">Metastore 是 SQL 資料庫，可用於儲存 Hive、Oozie 或兩者的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="a4b68-107">A metastore is a SQL Database that can used to store metadata for Hive, Oozie, or both.</span></span>

## <span data-ttu-id="a4b68-108">示例</span><span class="sxs-lookup"><span data-stu-id="a4b68-108">EXAMPLES</span></span>

### <span data-ttu-id="a4b68-109">範例1：新增 SQL 資料庫 metastore 至群集設定物件</span><span class="sxs-lookup"><span data-stu-id="a4b68-109">Example 1: Add a SQL database metastore to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
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
                -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageContainer
```

<span data-ttu-id="a4b68-110">這個命令會將 SQL 資料庫 metastore 新增到名為 [您的 hadoop-001] 的群集中。</span><span class="sxs-lookup"><span data-stu-id="a4b68-110">This command adds a SQL database metastore to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="a4b68-111">參數</span><span class="sxs-lookup"><span data-stu-id="a4b68-111">PARAMETERS</span></span>

### <span data-ttu-id="a4b68-112">-Config</span><span class="sxs-lookup"><span data-stu-id="a4b68-112">-Config</span></span>
<span data-ttu-id="a4b68-113">指定此 Cmdlet 修改的 HDInsight 群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="a4b68-113">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="a4b68-114">這個物件是由 **新的-AzHDInsightClusterConfig** Cmdlet 建立的。</span><span class="sxs-lookup"><span data-stu-id="a4b68-114">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="a4b68-115">-認證</span><span class="sxs-lookup"><span data-stu-id="a4b68-115">-Credential</span></span>
<span data-ttu-id="a4b68-116">指定要用於 AzureSQL 伺服器資料庫的認證。</span><span class="sxs-lookup"><span data-stu-id="a4b68-116">Specifies the credentials to use for the AzureSQL Server database.</span></span>

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

### <span data-ttu-id="a4b68-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a4b68-117">-DatabaseName</span></span>
<span data-ttu-id="a4b68-118">指定要用於此 metastore 的 AzureSQL 伺服器實例上的資料庫。</span><span class="sxs-lookup"><span data-stu-id="a4b68-118">Specifies the database on the AzureSQL Server instance to use for this metastore.</span></span>

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

### <span data-ttu-id="a4b68-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4b68-119">-DefaultProfile</span></span>
<span data-ttu-id="a4b68-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a4b68-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4b68-121">-MetastoreType</span><span class="sxs-lookup"><span data-stu-id="a4b68-121">-MetastoreType</span></span>
<span data-ttu-id="a4b68-122">指定 metastore 的類型。</span><span class="sxs-lookup"><span data-stu-id="a4b68-122">Specifies the type of metastore.</span></span>
<span data-ttu-id="a4b68-123">可能的值為 HiveMetastore 或 OozieMetastore。</span><span class="sxs-lookup"><span data-stu-id="a4b68-123">Possible values are HiveMetastore or OozieMetastore.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastoreType
Parameter Sets: (All)
Aliases:
Accepted values: HiveMetastore, OozieMetastore

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4b68-124">-SqlAzureServerName</span><span class="sxs-lookup"><span data-stu-id="a4b68-124">-SqlAzureServerName</span></span>
<span data-ttu-id="a4b68-125">指定要用於此 metastore 的 AzureSQL 伺服器實例。</span><span class="sxs-lookup"><span data-stu-id="a4b68-125">Specifies the AzureSQL Server instance to use for this metastore.</span></span>

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

### <span data-ttu-id="a4b68-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4b68-126">CommonParameters</span></span>
<span data-ttu-id="a4b68-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a4b68-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4b68-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a4b68-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4b68-129">輸入</span><span class="sxs-lookup"><span data-stu-id="a4b68-129">INPUTS</span></span>

### <span data-ttu-id="a4b68-130">AzureHDInsightConfig （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="a4b68-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="a4b68-131">輸出</span><span class="sxs-lookup"><span data-stu-id="a4b68-131">OUTPUTS</span></span>

### <span data-ttu-id="a4b68-132">AzureHDInsightConfig （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="a4b68-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="a4b68-133">筆記</span><span class="sxs-lookup"><span data-stu-id="a4b68-133">NOTES</span></span>

## <span data-ttu-id="a4b68-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="a4b68-134">RELATED LINKS</span></span>

[<span data-ttu-id="a4b68-135">新-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="a4b68-135">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


