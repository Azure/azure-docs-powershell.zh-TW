---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: FF8AA7DE-1E0F-4F5B-95F6-7820AAF789F2
online version: ''
schema: 2.0.0
ms.openlocfilehash: c36931af0b6927ef4fee26b9f8ade7db77d17db2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967366"
---
# <span data-ttu-id="ddc69-101">New-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="ddc69-101">New-AzureHDInsightClusterConfig</span></span>

## <span data-ttu-id="ddc69-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ddc69-102">SYNOPSIS</span></span>
<span data-ttu-id="ddc69-103">建立非持久化 HDInsight 群集配置。</span><span class="sxs-lookup"><span data-stu-id="ddc69-103">Creates a non-persisted HDInsight cluster configuration.</span></span>

## <span data-ttu-id="ddc69-104">句法</span><span class="sxs-lookup"><span data-stu-id="ddc69-104">SYNTAX</span></span>

```
New-AzureHDInsightClusterConfig -ClusterSizeInNodes <Int32> [-HeadNodeVMSize <String>]
 [-ClusterType <ClusterType>] [-VirtualNetworkId <String>] [-SubnetName <String>] [-DataNodeVMSize <String>]
 [-ZookeeperNodeVMSize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ddc69-105">說明</span><span class="sxs-lookup"><span data-stu-id="ddc69-105">DESCRIPTION</span></span>
<span data-ttu-id="ddc69-106">此版本的 Azure PowerShell HDInsight 已被否決。</span><span class="sxs-lookup"><span data-stu-id="ddc69-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="ddc69-107">這些 Cmdlet 將會在2017年1月1日移除。</span><span class="sxs-lookup"><span data-stu-id="ddc69-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="ddc69-108">請使用較新版本的 Azure PowerShell HDInsight。</span><span class="sxs-lookup"><span data-stu-id="ddc69-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="ddc69-109">如需如何使用新的 HDInsight 建立群集的相關資訊，請參閱 [使用 Azure PowerShell (在 HDInsight 中建立以 Linux 為基礎的群集](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 。</span><span class="sxs-lookup"><span data-stu-id="ddc69-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="ddc69-110">如需如何使用 Azure PowerShell 和其他方法提交作業的相關資訊，請參閱 [在 HDInsight 中提交 Hadoop 作業](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) 。</span><span class="sxs-lookup"><span data-stu-id="ddc69-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="ddc69-111">如需有關 Azure PowerShell HDInsight 的參考資訊，請參閱 [Azure HDInsight Cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="ddc69-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="ddc69-112">**新的-AzureHDInsightClusterConfig** Cmdlet 會建立非持久化 Azure HDInsight 群集配置。</span><span class="sxs-lookup"><span data-stu-id="ddc69-112">The **New-AzureHDInsightClusterConfig** cmdlet creates a non-persisted Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="ddc69-113">示例</span><span class="sxs-lookup"><span data-stu-id="ddc69-113">EXAMPLES</span></span>

### <span data-ttu-id="ddc69-114">範例1：建立群集設定</span><span class="sxs-lookup"><span data-stu-id="ddc69-114">Example 1: Create a cluster configuration</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $Key1 = Get-AzureStorageKey -StorageAccountName "MyBlobStorage" | %{ $_.Primary }
PS C:\> $Key2 = Get-AzureStorageKey -StorageAccountName "MySecondBlobStorage" | %{ $_.Primary }
PS C:\> $Creds = Get-Credential
PS C:\> $OozieCreds = Get-Credential
PS C:\> $HiveCreds = Get-Credential
PS C:\> New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4 
    | Set-AzureHDInsightDefaultStorage -StorageAccountName MyBlobStorage.blob.core.windows.net -StorageAccountKey $Key1 -StorageContainerName "MyContainer" 
    | Add-AzureHDInsightStorage -StorageAccountName "MySecondBlobStorage.blob.core.windows.net" -StorageAccountKey $Key2 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.windows.net" -DatabaseName "MyOozieDatabaseName" -Credential $OozieCreds -MetastoreType OozieMetastore 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.widows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore 
    | New-AzureHDInsightCluster -Subscription $SubID -Credential $Creds
```

<span data-ttu-id="ddc69-115">第一個命令使用 **AzureSubscription** Cmdlet 來取得目前的訂閱識別碼，然後將它儲存在 $SubId 變數中。</span><span class="sxs-lookup"><span data-stu-id="ddc69-115">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="ddc69-116">第二個和第三個命令使用 **AzureStorageKey** Cmdlet 來取得 MyBlobStorage 和 MySecondBlobStorage 的主要儲存空間，然後分別將金鑰儲存在 $Key 1 和 $Key 2 變數中。</span><span class="sxs-lookup"><span data-stu-id="ddc69-116">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="ddc69-117">第四個、第五個和第六個命令使用 **取得認證** Cmdlet 來取得目前訂閱與 Oozie 和 Hive 的認證，然後將認證儲存在變數中。</span><span class="sxs-lookup"><span data-stu-id="ddc69-117">The fourth, fifth, and sixth commands use the **Get-Credential** cmdlet to get credentials for the current subscription and for Oozie and Hive, and then store the credentials in variables.</span></span>

<span data-ttu-id="ddc69-118">最終命令會使用這些 Cmdlet 執行一系列的作業：</span><span class="sxs-lookup"><span data-stu-id="ddc69-118">The final command performs a sequence of operations by using these cmdlets:</span></span> 

- <span data-ttu-id="ddc69-119">[ **新增-AzureHDInsightClusterConfig** ] 可建立 HDInsight 群集設定。</span><span class="sxs-lookup"><span data-stu-id="ddc69-119">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration.</span></span>
- <span data-ttu-id="ddc69-120">**設定-AzureHDInsightDefaultStorage** ，將配置的預設儲存空間帳戶設定為 MyBlobStorage.blob.core.windows.net。</span><span class="sxs-lookup"><span data-stu-id="ddc69-120">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net.</span></span>
- <span data-ttu-id="ddc69-121">[ **載入 AzureHDInsightStorage** ]，將名為 MySecondBlobStorage.blob.core.windows.net 的第二個儲存空間帳戶新增至設定。</span><span class="sxs-lookup"><span data-stu-id="ddc69-121">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration.</span></span>
- <span data-ttu-id="ddc69-122">[ **AzureHDInsightMetastore** ]，將 Oozie 的 Metastore 和 Hive 的 metastore 設定為 [配置]。</span><span class="sxs-lookup"><span data-stu-id="ddc69-122">**Add-AzureHDInsightMetastore** to add a metastore for Oozie and a metastore for Hive to the configuration.</span></span>
- <span data-ttu-id="ddc69-123">[ **新增-AzureHDInsightCluster** ] 以使用新的設定建立 HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="ddc69-123">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration.</span></span>

## <span data-ttu-id="ddc69-124">參數</span><span class="sxs-lookup"><span data-stu-id="ddc69-124">PARAMETERS</span></span>

### <span data-ttu-id="ddc69-125">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="ddc69-125">-ClusterSizeInNodes</span></span>
<span data-ttu-id="ddc69-126">指定要為群集建立的資料節點數。</span><span class="sxs-lookup"><span data-stu-id="ddc69-126">Specifies the number of data nodes to create for a cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: Nodes, Size

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddc69-127">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="ddc69-127">-ClusterType</span></span>
<span data-ttu-id="ddc69-128">指定要建立的群集類型。</span><span class="sxs-lookup"><span data-stu-id="ddc69-128">Specifies the type of cluster to create.</span></span>

```yaml
Type: ClusterType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddc69-129">-DataNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="ddc69-129">-DataNodeVMSize</span></span>
<span data-ttu-id="ddc69-130">指定資料節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="ddc69-130">Specifies the size of the virtual machine for the data node.</span></span>

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

### <span data-ttu-id="ddc69-131">-HeadNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="ddc69-131">-HeadNodeVMSize</span></span>
<span data-ttu-id="ddc69-132">指定群集之頭節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="ddc69-132">Specifies the virtual machine size of the head node for the cluster.</span></span>

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

### <span data-ttu-id="ddc69-133">-設定檔</span><span class="sxs-lookup"><span data-stu-id="ddc69-133">-Profile</span></span>
<span data-ttu-id="ddc69-134">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="ddc69-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ddc69-135">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="ddc69-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ddc69-136">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="ddc69-136">-SubnetName</span></span>
<span data-ttu-id="ddc69-137">指定子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="ddc69-137">Specifies the name of a subnet.</span></span>

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

### <span data-ttu-id="ddc69-138">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="ddc69-138">-VirtualNetworkId</span></span>
<span data-ttu-id="ddc69-139">指定要在其中提供群集的虛擬網路識別碼。</span><span class="sxs-lookup"><span data-stu-id="ddc69-139">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="ddc69-140">-ZookeeperNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="ddc69-140">-ZookeeperNodeVMSize</span></span>
<span data-ttu-id="ddc69-141">指定 HBase 或風暴群集之 ZooKeeper 節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="ddc69-141">Specifies the size of the virtual machine for the ZooKeeper node for an HBase or Storm cluster.</span></span>

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

### <span data-ttu-id="ddc69-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddc69-142">CommonParameters</span></span>
<span data-ttu-id="ddc69-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ddc69-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddc69-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ddc69-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddc69-145">輸入</span><span class="sxs-lookup"><span data-stu-id="ddc69-145">INPUTS</span></span>

## <span data-ttu-id="ddc69-146">輸出</span><span class="sxs-lookup"><span data-stu-id="ddc69-146">OUTPUTS</span></span>

## <span data-ttu-id="ddc69-147">筆記</span><span class="sxs-lookup"><span data-stu-id="ddc69-147">NOTES</span></span>

## <span data-ttu-id="ddc69-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="ddc69-148">RELATED LINKS</span></span>

[<span data-ttu-id="ddc69-149">附加 AzureHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="ddc69-149">Add-AzureHDInsightMetastore</span></span>](./Add-AzureHDInsightMetastore.md)

[<span data-ttu-id="ddc69-150">附加 AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="ddc69-150">Add-AzureHDInsightStorage</span></span>](./Add-AzureHDInsightStorage.md)

[<span data-ttu-id="ddc69-151">新-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="ddc69-151">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="ddc69-152">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="ddc69-152">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)


