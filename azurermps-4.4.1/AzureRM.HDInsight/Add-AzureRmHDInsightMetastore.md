---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 8BD3B8BD-DC87-4A94-9FCA-611D11D5E065
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightMetastore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightMetastore.md
ms.openlocfilehash: f21108e949ff1d6787488f9f4b6c062d5954a7e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455823"
---
# <span data-ttu-id="3b406-101">Add-AzureRmHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="3b406-101">Add-AzureRmHDInsightMetastore</span></span>

## <span data-ttu-id="3b406-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3b406-102">SYNOPSIS</span></span>
<span data-ttu-id="3b406-103">新增 SQL 資料庫，以作為 Hive 或 Oozie metastore 至群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="3b406-103">Adds a SQL Database to serve as a Hive or Oozie metastore to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b406-104">句法</span><span class="sxs-lookup"><span data-stu-id="3b406-104">SYNTAX</span></span>

```
Add-AzureRmHDInsightMetastore [-Config] <AzureHDInsightConfig> [-MetastoreType] <AzureHDInsightMetastoreType>
 [-SqlAzureServerName] <String> [-DatabaseName] <String> [-Credential] <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b406-105">說明</span><span class="sxs-lookup"><span data-stu-id="3b406-105">DESCRIPTION</span></span>
<span data-ttu-id="3b406-106">**AzureRmHDInsightMetastore** Cmdlet 會將 Hive 或 Oozie metastore 新增至 New-AzureRmHDInsightClusterConfig Cmdlet 建立的 HDInsight 設定物件。</span><span class="sxs-lookup"><span data-stu-id="3b406-106">The **Add-AzureRmHDInsightMetastore** cmdlet adds a Hive or Oozie metastore to the HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>
<span data-ttu-id="3b406-107">Metastore 是 SQL 資料庫，可用於儲存 Hive、Oozie 或兩者的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="3b406-107">A metastore is a SQL Database that can used to store metadata for Hive, Oozie, or both.</span></span>

## <span data-ttu-id="3b406-108">示例</span><span class="sxs-lookup"><span data-stu-id="3b406-108">EXAMPLES</span></span>

### <span data-ttu-id="3b406-109">範例1：新增 SQL 資料庫 metastore 至群集設定物件</span><span class="sxs-lookup"><span data-stu-id="3b406-109">Example 1: Add a SQL database metastore to the cluster configuration object</span></span>
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

# Hive metastore info
PS C:\> $hiveSqlServer = "your-sqlserver-001"
PS C:\> $hiveDb = "your-sqldb-001"
PS C:\> $hiveCreds = Get-Credential

# Oozie metastore info
PS C:\> $oozieSqlServer = "your-sqlserver-001"
PS C:\> $oozieDb = "your-sqldb-002"
PS C:\> $oozieCreds = Get-Credential

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig  `
            | Add-AzureRmHDInsightMetastore `
                -SqlAzureServerName "$oozieSqlServer.database.contoso.net" `
                -DatabaseName $oozieDb `
                -Credential $oozieCreds `
                -MetastoreType OozieMetastore `
            | Add-AzureRmHDInsightMetastore `
                -SqlAzureServerName "$hiveSqlServer.database.contoso.net" `
                -DatabaseName $hiveDb `
                -Credential $hiveCreds `
                -MetastoreType HiveMetastore `
            | New-AzureRmHDInsightCluster `
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

<span data-ttu-id="3b406-110">這個命令會將 SQL 資料庫 metastore 新增到名為 [您的 hadoop-001] 的群集中。</span><span class="sxs-lookup"><span data-stu-id="3b406-110">This command adds a SQL database metastore to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="3b406-111">參數</span><span class="sxs-lookup"><span data-stu-id="3b406-111">PARAMETERS</span></span>

### <span data-ttu-id="3b406-112">-Config</span><span class="sxs-lookup"><span data-stu-id="3b406-112">-Config</span></span>
<span data-ttu-id="3b406-113">指定此 Cmdlet 修改的 HDInsight 群集設定物件。</span><span class="sxs-lookup"><span data-stu-id="3b406-113">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="3b406-114">這個物件是由 **新的-AzureRmHDInsightClusterConfig** Cmdlet 建立的。</span><span class="sxs-lookup"><span data-stu-id="3b406-114">This object is created by the **New-AzureRmHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="3b406-115">-認證</span><span class="sxs-lookup"><span data-stu-id="3b406-115">-Credential</span></span>
<span data-ttu-id="3b406-116">指定要用於 AzureSQL 伺服器資料庫的認證。</span><span class="sxs-lookup"><span data-stu-id="3b406-116">Specifies the credentials to use for the AzureSQL Server database.</span></span>

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

### <span data-ttu-id="3b406-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3b406-117">-DatabaseName</span></span>
<span data-ttu-id="3b406-118">指定要用於此 metastore 的 AzureSQL 伺服器實例上的資料庫。</span><span class="sxs-lookup"><span data-stu-id="3b406-118">Specifies the database on the AzureSQL Server instance to use for this metastore.</span></span>

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

### <span data-ttu-id="3b406-119">-MetastoreType</span><span class="sxs-lookup"><span data-stu-id="3b406-119">-MetastoreType</span></span>
<span data-ttu-id="3b406-120">指定 metastore 的類型。</span><span class="sxs-lookup"><span data-stu-id="3b406-120">Specifies the type of metastore.</span></span>
<span data-ttu-id="3b406-121">可能的值為 HiveMetastore 或 OozieMetastore。</span><span class="sxs-lookup"><span data-stu-id="3b406-121">Possible values are HiveMetastore or OozieMetastore.</span></span>

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

### <span data-ttu-id="3b406-122">-SqlAzureServerName</span><span class="sxs-lookup"><span data-stu-id="3b406-122">-SqlAzureServerName</span></span>
<span data-ttu-id="3b406-123">指定要用於此 metastore 的 AzureSQL 伺服器實例。</span><span class="sxs-lookup"><span data-stu-id="3b406-123">Specifies the AzureSQL Server instance to use for this metastore.</span></span>

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

### <span data-ttu-id="3b406-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b406-124">-DefaultProfile</span></span>
<span data-ttu-id="3b406-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3b406-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b406-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b406-126">CommonParameters</span></span>
<span data-ttu-id="3b406-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3b406-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b406-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3b406-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b406-129">輸入</span><span class="sxs-lookup"><span data-stu-id="3b406-129">INPUTS</span></span>

### <span data-ttu-id="3b406-130">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="3b406-130">AzureHDInsightConfig</span></span>
<span data-ttu-id="3b406-131">形參 "Config" 接受管線中 "AzureHDInsightConfig" 類型的值</span><span class="sxs-lookup"><span data-stu-id="3b406-131">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="3b406-132">輸出</span><span class="sxs-lookup"><span data-stu-id="3b406-132">OUTPUTS</span></span>

### <span data-ttu-id="3b406-133">AzureHDInsightConfig （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="3b406-133">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="3b406-134">筆記</span><span class="sxs-lookup"><span data-stu-id="3b406-134">NOTES</span></span>

## <span data-ttu-id="3b406-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="3b406-135">RELATED LINKS</span></span>

[<span data-ttu-id="3b406-136">新-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="3b406-136">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)


