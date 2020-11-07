---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 3EDD612F-AC5D-4D4D-BB14-2FB8DE5EDCCE
online version: ''
schema: 2.0.0
ms.openlocfilehash: a4652cb1b30717b5ea11d596646dc43e2a5ec4a0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967369"
---
# <span data-ttu-id="59bb9-101">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="59bb9-101">New-AzureHDInsightCluster</span></span>

## <span data-ttu-id="59bb9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="59bb9-102">SYNOPSIS</span></span>
<span data-ttu-id="59bb9-103">建立 HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="59bb9-103">Creates an HDInsight cluster.</span></span>

## <span data-ttu-id="59bb9-104">句法</span><span class="sxs-lookup"><span data-stu-id="59bb9-104">SYNTAX</span></span>

### <span data-ttu-id="59bb9-105">群集依據 Config (使用特定的訂閱認證)  (預設) </span><span class="sxs-lookup"><span data-stu-id="59bb9-105">Cluster By Config (with Specific Subscription Credential) (Default)</span></span>
```
New-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>]
 -Config <AzureHDInsightConfig> -Credential <PSCredential> [-EndPoint <Uri>] [-IgnoreSslErrors <Boolean>]
 -Location <String> -Name <String> [-Subscription <String>] [-Version <String>] [-OSType <OSType>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="59bb9-106">群集依名稱 (與特定的訂閱認證) </span><span class="sxs-lookup"><span data-stu-id="59bb9-106">Cluster By Name (with Specific Subscription Credential)</span></span>
```
New-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>]
 -ClusterSizeInNodes <Int32> -Credential <PSCredential> -DefaultStorageAccountKey <String>
 -DefaultStorageAccountName <String> -DefaultStorageContainerName <String> [-EndPoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Location <String> -Name <String> [-Subscription <String>] [-Version <String>]
 [-HeadNodeVMSize <String>] [-ClusterType <ClusterType>] [-VirtualNetworkId <String>] [-SubnetName <String>]
 [-DataNodeVMSize <String>] [-ZookeeperNodeVMSize <String>] [-OSType <OSType>] [-SshCredential <PSCredential>]
 [-SshPublicKey <String>] [-RdpCredential <PSCredential>] [-RdpAccessExpiry <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="59bb9-107">說明</span><span class="sxs-lookup"><span data-stu-id="59bb9-107">DESCRIPTION</span></span>
<span data-ttu-id="59bb9-108">此版本的 Azure PowerShell HDInsight 已被否決。</span><span class="sxs-lookup"><span data-stu-id="59bb9-108">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="59bb9-109">這些 Cmdlet 將會在2017年1月1日移除。</span><span class="sxs-lookup"><span data-stu-id="59bb9-109">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="59bb9-110">請使用較新版本的 Azure PowerShell HDInsight。</span><span class="sxs-lookup"><span data-stu-id="59bb9-110">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="59bb9-111">如需如何使用新的 HDInsight 建立群集的相關資訊，請參閱 [使用 Azure PowerShell (在 HDInsight 中建立以 Linux 為基礎的群集](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 。</span><span class="sxs-lookup"><span data-stu-id="59bb9-111">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="59bb9-112">如需如何使用 Azure PowerShell 和其他方法提交作業的相關資訊，請參閱 [在 HDInsight 中提交 Hadoop 作業](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) 。</span><span class="sxs-lookup"><span data-stu-id="59bb9-112">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="59bb9-113">如需有關 Azure PowerShell HDInsight 的參考資訊，請參閱 [Azure HDInsight Cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="59bb9-113">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="59bb9-114">**AzureHDInsightCluster** Cmdlet 會使用指定的參數來建立 Azure HDInsight 群集，或使用使用 **New-AzureHDInsightClusterConfig** Cmdlet 建立的 configuration 物件來建立。</span><span class="sxs-lookup"><span data-stu-id="59bb9-114">The **New-AzureHDInsightCluster** cmdlet creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the **New-AzureHDInsightClusterConfig** cmdlet.</span></span>

## <span data-ttu-id="59bb9-115">示例</span><span class="sxs-lookup"><span data-stu-id="59bb9-115">EXAMPLES</span></span>

### <span data-ttu-id="59bb9-116">範例1：建立 HDInsight 群集</span><span class="sxs-lookup"><span data-stu-id="59bb9-116">Example 1: Create an HDInsight cluster</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $Key1 = Get-AzureStorageKey -StorageAccountName "MyBlobStorage" | %{ $_.Primary }
PS C:\> $Key2 = Get-AzureStorageKey -StorageAccountName "MySecondBlobStorage" | %{ $_.Primary }
PS C:\> $Creds = Get-Credential
PS C:\> $OozieCreds = Get-Credential
PS C:\> $HiveCreds = Get-Credential 
PS C:\> New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4 
    | Set-AzureHDInsightDefaultStorage -StorageAccountName "MyBlobStorage.blob.core.windows.net" -StorageAccountKey $Key1 -StorageContainerName "MyContainer" 
    | Add-AzureHDInsightStorage -StorageAccountName "MySecondBlobStorage.blob.core.windows.net" -StorageAccountKey $Key2 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.windows.net" -DatabaseName "MyOozieDatabaseName" -Credential $OozieCreds -MetastoreType OozieMetastore 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.windows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore 
    | New-AzureHDInsightCluster -Subscription $SubId -Credential $Creds
```

<span data-ttu-id="59bb9-117">這個範例會為目前的訂閱建立 HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="59bb9-117">This example creates an HDInsight cluster for the current subscription.</span></span>

<span data-ttu-id="59bb9-118">第一個命令使用 **AzureSubscription** Cmdlet 來取得目前的訂閱識別碼，然後將它儲存在 $SubId 變數中。</span><span class="sxs-lookup"><span data-stu-id="59bb9-118">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="59bb9-119">第二個和第三個命令使用 **AzureStorageKey** Cmdlet 來取得 MyBlobStorage 和 MySecondBlobStorage 的主要儲存空間，然後分別將金鑰儲存在 $Key 1 和 $Key 2 變數中。</span><span class="sxs-lookup"><span data-stu-id="59bb9-119">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="59bb9-120">第四個、第五個和第六個命令使用 **取得認證** Cmdlet 來取得目前訂閱與 Oozie 和 Hive 的認證，然後將認證儲存在變數中。</span><span class="sxs-lookup"><span data-stu-id="59bb9-120">The fourth, fifth, and sixth commands use the **Get-Credential** cmdlet to get credentials for the current subscription and for Oozie and Hive, and then store the credentials in variables.</span></span>

<span data-ttu-id="59bb9-121">最終命令會使用這些 Cmdlet 執行一系列的作業：</span><span class="sxs-lookup"><span data-stu-id="59bb9-121">The final command performs a sequence of operations by using these cmdlets:</span></span>

- <span data-ttu-id="59bb9-122">[ **新增-AzureHDInsightClusterConfig** ] 可建立 HDInsight 群集設定。</span><span class="sxs-lookup"><span data-stu-id="59bb9-122">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration.</span></span>
- <span data-ttu-id="59bb9-123">**設定-AzureHDInsightDefaultStorage** ，將配置的預設儲存空間帳戶設定為 MyBlobStorage.blob.core.windows.net。</span><span class="sxs-lookup"><span data-stu-id="59bb9-123">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net.</span></span>
- <span data-ttu-id="59bb9-124">[ **載入 AzureHDInsightStorage** ]，將名為 MySecondBlobStorage.blob.core.windows.net 的第二個儲存空間帳戶新增至設定。</span><span class="sxs-lookup"><span data-stu-id="59bb9-124">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration.</span></span>
- <span data-ttu-id="59bb9-125">[ **AzureHDInsightMetastore** ]，將 Oozie 的 Metastore 和 Hive 的 metastore 設定為 [配置]。</span><span class="sxs-lookup"><span data-stu-id="59bb9-125">**Add-AzureHDInsightMetastore** to add a metastore for Oozie and a metastore for Hive to the configuration.</span></span>
- <span data-ttu-id="59bb9-126">[ **新增-AzureHDInsightCluster** ] 以使用新的設定建立 HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="59bb9-126">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration.</span></span>

## <span data-ttu-id="59bb9-127">參數</span><span class="sxs-lookup"><span data-stu-id="59bb9-127">PARAMETERS</span></span>

### <span data-ttu-id="59bb9-128">-Certificate</span><span class="sxs-lookup"><span data-stu-id="59bb9-128">-Certificate</span></span>
<span data-ttu-id="59bb9-129">指定 Azure 訂閱的管理憑證。</span><span class="sxs-lookup"><span data-stu-id="59bb9-129">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: (All)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59bb9-130">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="59bb9-130">-ClusterSizeInNodes</span></span>
<span data-ttu-id="59bb9-131">指定要為群集建立的資料節點數。</span><span class="sxs-lookup"><span data-stu-id="59bb9-131">Specifies the number of data nodes to create for a cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: Nodes, Size

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59bb9-132">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="59bb9-132">-ClusterType</span></span>
<span data-ttu-id="59bb9-133">指定要建立的群集類型。</span><span class="sxs-lookup"><span data-stu-id="59bb9-133">Specifies the type of cluster to create.</span></span>

```yaml
Type: ClusterType
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59bb9-134">-Config</span><span class="sxs-lookup"><span data-stu-id="59bb9-134">-Config</span></span>
<span data-ttu-id="59bb9-135">指定使用 **New-AzureHDInsightClusterConfig** Cmdlet 建立的設定物件。</span><span class="sxs-lookup"><span data-stu-id="59bb9-135">Specifies a configuration object that is created by using the **New-AzureHDInsightClusterConfig** cmdlet.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: Cluster By Config (with Specific Subscription Credential)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59bb9-136">-認證</span><span class="sxs-lookup"><span data-stu-id="59bb9-136">-Credential</span></span>
<span data-ttu-id="59bb9-137">指定供 HDInsight 使用的使用者認證，以用於遠端存取 Hadoop 群集的預設帳戶。</span><span class="sxs-lookup"><span data-stu-id="59bb9-137">Specifies the user credentials for HDInsight to use for the default account that is used to remotely access a Hadoop cluster.</span></span>
<span data-ttu-id="59bb9-138">這些認證與使用者的訂閱認證不同。</span><span class="sxs-lookup"><span data-stu-id="59bb9-138">These credentials are distinct from the subscription credentials of the user.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: Cred

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59bb9-139">-DataNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="59bb9-139">-DataNodeVMSize</span></span>
<span data-ttu-id="59bb9-140">指定資料節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="59bb9-140">Specifies the size of the virtual machine for the data node.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59bb9-141">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="59bb9-141">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="59bb9-142">指定 HDInsight 群集使用之預設儲存空間帳戶的帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="59bb9-142">Specifies the account key for the default storage account that the HDInsight cluster uses.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: StorageKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59bb9-143">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="59bb9-143">-DefaultStorageAccountName</span></span>
<span data-ttu-id="59bb9-144">指定 HDInsight 群集使用的預設儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="59bb9-144">Specifies the name of the default storage account that the HDInsight cluster uses.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: StorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59bb9-145">-DefaultStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="59bb9-145">-DefaultStorageContainerName</span></span>
<span data-ttu-id="59bb9-146">指定 HDInsight 群集使用的預設 Azure 儲存空間帳戶中預設容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="59bb9-146">Specifies the name of the default container in the default Azure storage account that an HDInsight cluster uses.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: StorageContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59bb9-147">-端點</span><span class="sxs-lookup"><span data-stu-id="59bb9-147">-EndPoint</span></span>
<span data-ttu-id="59bb9-148">指定要用來連接 Azure 的端點。</span><span class="sxs-lookup"><span data-stu-id="59bb9-148">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="59bb9-149">如果您沒有指定此參數，此 Cmdlet 會使用預設端點。</span><span class="sxs-lookup"><span data-stu-id="59bb9-149">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59bb9-150">-HeadNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="59bb9-150">-HeadNodeVMSize</span></span>
<span data-ttu-id="59bb9-151">指定頭節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="59bb9-151">Specifies the size of the virtual machine for the head node.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59bb9-152">-HostedService</span><span class="sxs-lookup"><span data-stu-id="59bb9-152">-HostedService</span></span>
<span data-ttu-id="59bb9-153">指定 HDInsight 服務的命名空間。</span><span class="sxs-lookup"><span data-stu-id="59bb9-153">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="59bb9-154">如果您沒有指定此參數，這個 Cmdlet 會使用預設的命名空間。</span><span class="sxs-lookup"><span data-stu-id="59bb9-154">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59bb9-155">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="59bb9-155">-IgnoreSslErrors</span></span>
<span data-ttu-id="59bb9-156">指出是否已忽略安全通訊端層 (SSL) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="59bb9-156">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59bb9-157">-位置</span><span class="sxs-lookup"><span data-stu-id="59bb9-157">-Location</span></span>
<span data-ttu-id="59bb9-158">指定要在其中建立 HDInsight 群集的區域。</span><span class="sxs-lookup"><span data-stu-id="59bb9-158">Specifies the region in which to create an HDInsight cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Loc

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59bb9-159">-名稱</span><span class="sxs-lookup"><span data-stu-id="59bb9-159">-Name</span></span>
<span data-ttu-id="59bb9-160">指定要建立之 Azure HDInsight 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="59bb9-160">Specifies the name of the Azure HDInsight cluster to create.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Config (with Specific Subscription Credential)
Aliases: ClusterName, DnsName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: ClusterName, DnsName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59bb9-161">-OSType</span><span class="sxs-lookup"><span data-stu-id="59bb9-161">-OSType</span></span>
<span data-ttu-id="59bb9-162">指定群集的作業系統。</span><span class="sxs-lookup"><span data-stu-id="59bb9-162">Specifies the operating system for a cluster.</span></span>

```yaml
Type: OSType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59bb9-163">-設定檔</span><span class="sxs-lookup"><span data-stu-id="59bb9-163">-Profile</span></span>
<span data-ttu-id="59bb9-164">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="59bb9-164">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="59bb9-165">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="59bb9-165">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="59bb9-166">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="59bb9-166">-RdpAccessExpiry</span></span>
<span data-ttu-id="59bb9-167">指定遠端桌面通訊協定的到期日（例如 **DateTime** 物件） (RDP) 對群集的存取權。</span><span class="sxs-lookup"><span data-stu-id="59bb9-167">Specifies the expiration, as a **DateTime** object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59bb9-168">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="59bb9-168">-RdpCredential</span></span>
<span data-ttu-id="59bb9-169">指定 RDP 存取群集的認證。</span><span class="sxs-lookup"><span data-stu-id="59bb9-169">Specifies the credentials for RDP access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59bb9-170">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="59bb9-170">-SshCredential</span></span>
<span data-ttu-id="59bb9-171">指定 HDInsight 群集的 (SSH) 使用者名稱和密碼的安全 Shell。</span><span class="sxs-lookup"><span data-stu-id="59bb9-171">Specifies the Secure Shell (SSH) user name and password for the HDInsight cluster.</span></span>
<span data-ttu-id="59bb9-172">這個參數只對 Linux 群集有效。</span><span class="sxs-lookup"><span data-stu-id="59bb9-172">This parameter is valid only for Linux clusters.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59bb9-173">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="59bb9-173">-SshPublicKey</span></span>
<span data-ttu-id="59bb9-174">指定 HDInsight 群集的 SSH 公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="59bb9-174">Specifies the SSH public key for an HDInsight cluster.</span></span>
<span data-ttu-id="59bb9-175">這個參數只對 Linux 群集有效。</span><span class="sxs-lookup"><span data-stu-id="59bb9-175">This parameter is valid only for Linux clusters.</span></span>

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

### <span data-ttu-id="59bb9-176">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="59bb9-176">-SubnetName</span></span>
<span data-ttu-id="59bb9-177">指定子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="59bb9-177">Specifies the name of a subnet.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59bb9-178">-訂閱</span><span class="sxs-lookup"><span data-stu-id="59bb9-178">-Subscription</span></span>
<span data-ttu-id="59bb9-179">指定要在其中建立 HDInsight 群集的 Azure 訂閱。</span><span class="sxs-lookup"><span data-stu-id="59bb9-179">Specifies the Azure subscription in which to create an HDInsight cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59bb9-180">-版本</span><span class="sxs-lookup"><span data-stu-id="59bb9-180">-Version</span></span>
<span data-ttu-id="59bb9-181">指定要建立的 HDInsight 群集版本。</span><span class="sxs-lookup"><span data-stu-id="59bb9-181">Specifies the HDInsight cluster version to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Ver

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59bb9-182">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="59bb9-182">-VirtualNetworkId</span></span>
<span data-ttu-id="59bb9-183">指定要在其中提供群集的虛擬網路識別碼。</span><span class="sxs-lookup"><span data-stu-id="59bb9-183">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59bb9-184">-ZookeeperNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="59bb9-184">-ZookeeperNodeVMSize</span></span>
<span data-ttu-id="59bb9-185">指定 ZooKeeper 節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="59bb9-185">Specifies the size of the virtual machine for the ZooKeeper node.</span></span>
<span data-ttu-id="59bb9-186">這個參數只對 HBase 或風暴群集有效。</span><span class="sxs-lookup"><span data-stu-id="59bb9-186">This parameter is valid only for HBase or Storm clusters.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59bb9-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59bb9-187">CommonParameters</span></span>
<span data-ttu-id="59bb9-188">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="59bb9-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59bb9-189">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="59bb9-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59bb9-190">輸入</span><span class="sxs-lookup"><span data-stu-id="59bb9-190">INPUTS</span></span>

## <span data-ttu-id="59bb9-191">輸出</span><span class="sxs-lookup"><span data-stu-id="59bb9-191">OUTPUTS</span></span>

## <span data-ttu-id="59bb9-192">筆記</span><span class="sxs-lookup"><span data-stu-id="59bb9-192">NOTES</span></span>

## <span data-ttu-id="59bb9-193">相關連結</span><span class="sxs-lookup"><span data-stu-id="59bb9-193">RELATED LINKS</span></span>

[<span data-ttu-id="59bb9-194">附加 AzureHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="59bb9-194">Add-AzureHDInsightMetastore</span></span>](./Add-AzureHDInsightMetastore.md)

[<span data-ttu-id="59bb9-195">附加 AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="59bb9-195">Add-AzureHDInsightStorage</span></span>](./Add-AzureHDInsightStorage.md)

[<span data-ttu-id="59bb9-196">AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="59bb9-196">Get-AzureHDInsightCluster</span></span>](./Get-AzureHDInsightCluster.md)

[<span data-ttu-id="59bb9-197">新-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="59bb9-197">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)

[<span data-ttu-id="59bb9-198">移除-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="59bb9-198">Remove-AzureHDInsightCluster</span></span>](./Remove-AzureHDInsightCluster.md)

[<span data-ttu-id="59bb9-199">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="59bb9-199">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)

[<span data-ttu-id="59bb9-200">使用-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="59bb9-200">Use-AzureHDInsightCluster</span></span>](./Use-AzureHDInsightCluster.md)


