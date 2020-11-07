---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: EB196CF5-3E2C-4F38-A983-3365A379672A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 637fc6f65c7168db9ba7e45cea7268208b334c99
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967169"
---
# <span data-ttu-id="e69c1-101">Add-AzureHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="e69c1-101">Add-AzureHDInsightMetastore</span></span>

## <span data-ttu-id="e69c1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e69c1-102">SYNOPSIS</span></span>
<span data-ttu-id="e69c1-103">將 SQL Server 資料庫帳戶新增至 HDInsight 群集設定。</span><span class="sxs-lookup"><span data-stu-id="e69c1-103">Adds a SQL Server database account to an HDInsight cluster configuration.</span></span>

## <span data-ttu-id="e69c1-104">句法</span><span class="sxs-lookup"><span data-stu-id="e69c1-104">SYNTAX</span></span>

```
Add-AzureHDInsightMetastore -Config <AzureHDInsightConfig> -Credential <PSCredential> -DatabaseName <String>
 -MetastoreType <AzureHDInsightMetastoreType> -SqlAzureServerName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="e69c1-105">說明</span><span class="sxs-lookup"><span data-stu-id="e69c1-105">DESCRIPTION</span></span>
<span data-ttu-id="e69c1-106">此版本的 Azure PowerShell HDInsight 已被否決。</span><span class="sxs-lookup"><span data-stu-id="e69c1-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="e69c1-107">這些 Cmdlet 將會在2017年1月1日移除。</span><span class="sxs-lookup"><span data-stu-id="e69c1-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="e69c1-108">請使用較新版本的 Azure PowerShell HDInsight。</span><span class="sxs-lookup"><span data-stu-id="e69c1-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="e69c1-109">如需如何使用新的 HDInsight 建立群集的相關資訊，請參閱 [使用 Azure PowerShell (在 HDInsight 中建立以 Linux 為基礎的群集](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 。</span><span class="sxs-lookup"><span data-stu-id="e69c1-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="e69c1-110">如需如何使用 Azure PowerShell 和其他方法提交作業的相關資訊，請參閱 [在 HDInsight 中提交 Hadoop 作業](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) 。</span><span class="sxs-lookup"><span data-stu-id="e69c1-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="e69c1-111">如需有關 Azure PowerShell HDInsight 的參考資訊，請參閱 [Azure HDInsight Cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="e69c1-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="e69c1-112">**AzureHDInsightMetastore** Cmdlet 會將 Microsoft SQL Server 資料庫新增至由 **新的-AzureHDInsightClusterConfig** Cmdlet 建立的 Azure HDInsight 配置。</span><span class="sxs-lookup"><span data-stu-id="e69c1-112">The **Add-AzureHDInsightMetastore** cmdlet adds a Microsoft SQL Server database to an Azure HDInsight configuration that is created by the **New-AzureHDInsightClusterConfig** cmdlet.</span></span>
<span data-ttu-id="e69c1-113">資料庫是用來儲存 Hive 或 Oozie 或兩者的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="e69c1-113">The database is used to store metadata for Hive or Oozie, or both.</span></span>

## <span data-ttu-id="e69c1-114">示例</span><span class="sxs-lookup"><span data-stu-id="e69c1-114">EXAMPLES</span></span>

### <span data-ttu-id="e69c1-115">範例1：新增 metastore</span><span class="sxs-lookup"><span data-stu-id="e69c1-115">Example 1: Add a metastore</span></span>
```
PS C:\>$Metaconfig = Add-AzureHDInsightMetastore -Config $Config -SqlAzureServerName "ContosoSQLServer" -DatabaseName "DBname" -Credential (Get-Credential) -MetastoreType HiveMetaStore
```

<span data-ttu-id="e69c1-116">這個命令會新增一個名為 ContosoSQLServer 的 SQL Server 資料庫，以充當 HDInsight 群集的 Hive metastore。</span><span class="sxs-lookup"><span data-stu-id="e69c1-116">This command adds a SQL Server database named ContosoSQLServer to serve as a Hive metastore for an HDInsight cluster.</span></span>

### <span data-ttu-id="e69c1-117">範例2：設定儲存空間並新增 metastores</span><span class="sxs-lookup"><span data-stu-id="e69c1-117">Example 2: Configure storage and add metastores</span></span>
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
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.widows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore
    | New-AzureHDInsightCluster -Subscription $SubId -Credential $Creds
```

<span data-ttu-id="e69c1-118">第一個命令使用 **AzureSubscription** Cmdlet 來取得目前的訂閱識別碼，然後將它儲存在 $SubId 變數中。</span><span class="sxs-lookup"><span data-stu-id="e69c1-118">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="e69c1-119">第二個和第三個命令使用 **AzureStorageKey** Cmdlet 來取得 MyBlobStorage 和 MySecondBlobStorage 的主要儲存空間，然後分別將金鑰儲存在 $Key 1 和 $Key 2 變數中。</span><span class="sxs-lookup"><span data-stu-id="e69c1-119">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="e69c1-120">第四個、第五個和第六個命令使用 **取得認證** Cmdlet 來取得目前訂閱與 Oozie 和 Hive 的認證，然後將認證儲存在變數中。</span><span class="sxs-lookup"><span data-stu-id="e69c1-120">The fourth, fifth, and sixth commands use the **Get-Credential** cmdlet to get credentials for the current subscription and for Oozie and Hive, and then store the credentials in variables.</span></span>

<span data-ttu-id="e69c1-121">最終命令會使用這些 Cmdlet 執行一系列的作業：</span><span class="sxs-lookup"><span data-stu-id="e69c1-121">The final command performs a sequence of operations by using these cmdlets:</span></span>

- <span data-ttu-id="e69c1-122">[ **新增-AzureHDInsightClusterConfig** ] 可建立 HDInsight 群集設定。</span><span class="sxs-lookup"><span data-stu-id="e69c1-122">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration.</span></span>
- <span data-ttu-id="e69c1-123">**設定-AzureHDInsightDefaultStorage** ，將配置的預設儲存空間帳戶設定為 MyBlobStorage.blob.core.windows.net。</span><span class="sxs-lookup"><span data-stu-id="e69c1-123">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net.</span></span>
- <span data-ttu-id="e69c1-124">[ **載入 AzureHDInsightStorage** ]，將名為 MySecondBlobStorage.blob.core.windows.net 的第二個儲存空間帳戶新增至設定。</span><span class="sxs-lookup"><span data-stu-id="e69c1-124">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration.</span></span>
- <span data-ttu-id="e69c1-125">[ **AzureHDInsightMetastore** ]，將 Oozie 的 Metastore 和 Hive 的 metastore 設定為 [配置]。</span><span class="sxs-lookup"><span data-stu-id="e69c1-125">**Add-AzureHDInsightMetastore** to add a metastore for Oozie and a metastore for Hive to the configuration.</span></span>
- <span data-ttu-id="e69c1-126">[ **新增-AzureHDInsightCluster** ] 以使用新的設定建立 HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="e69c1-126">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration.</span></span>

## <span data-ttu-id="e69c1-127">參數</span><span class="sxs-lookup"><span data-stu-id="e69c1-127">PARAMETERS</span></span>

### <span data-ttu-id="e69c1-128">-Config</span><span class="sxs-lookup"><span data-stu-id="e69c1-128">-Config</span></span>
<span data-ttu-id="e69c1-129">指定 [配置] 物件。</span><span class="sxs-lookup"><span data-stu-id="e69c1-129">Specifies a configuration object.</span></span>
<span data-ttu-id="e69c1-130">這個 Cmdlet 會將 metastore 資訊新增到此參數指定的設定物件。</span><span class="sxs-lookup"><span data-stu-id="e69c1-130">This cmdlet adds metastore information to the configuration object that this parameter specifies.</span></span>

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

### <span data-ttu-id="e69c1-131">-認證</span><span class="sxs-lookup"><span data-stu-id="e69c1-131">-Credential</span></span>
<span data-ttu-id="e69c1-132">指定用來存取 SQL Server 資料庫的認證。</span><span class="sxs-lookup"><span data-stu-id="e69c1-132">Specifies the credentials that are used to access a SQL Server database.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e69c1-133">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e69c1-133">-DatabaseName</span></span>
<span data-ttu-id="e69c1-134">指定要儲存 Hive 或 Oozie 中繼資料之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="e69c1-134">Specifies the name of the database to store Hive or Oozie metadata.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e69c1-135">-MetastoreType</span><span class="sxs-lookup"><span data-stu-id="e69c1-135">-MetastoreType</span></span>
<span data-ttu-id="e69c1-136">指定 metastore 類型。</span><span class="sxs-lookup"><span data-stu-id="e69c1-136">Specifies the metastore type.</span></span>
<span data-ttu-id="e69c1-137">此參數可接受的值為： HiveMetaStore 或 OozieMetaStore。</span><span class="sxs-lookup"><span data-stu-id="e69c1-137">The acceptable values for this parameter are: HiveMetaStore or OozieMetaStore.</span></span>

```yaml
Type: AzureHDInsightMetastoreType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e69c1-138">-設定檔</span><span class="sxs-lookup"><span data-stu-id="e69c1-138">-Profile</span></span>
<span data-ttu-id="e69c1-139">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="e69c1-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e69c1-140">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="e69c1-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e69c1-141">-SqlAzureServerName</span><span class="sxs-lookup"><span data-stu-id="e69c1-141">-SqlAzureServerName</span></span>
<span data-ttu-id="e69c1-142">指定包含用來儲存中繼資料之資料庫之 SQL Server (FQDN) 的完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="e69c1-142">Specifies the fully qualified domain name (FQDN) of the SQL Server that contains the database to store metadata.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e69c1-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e69c1-143">CommonParameters</span></span>
<span data-ttu-id="e69c1-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e69c1-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e69c1-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e69c1-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e69c1-146">輸入</span><span class="sxs-lookup"><span data-stu-id="e69c1-146">INPUTS</span></span>

## <span data-ttu-id="e69c1-147">輸出</span><span class="sxs-lookup"><span data-stu-id="e69c1-147">OUTPUTS</span></span>

## <span data-ttu-id="e69c1-148">筆記</span><span class="sxs-lookup"><span data-stu-id="e69c1-148">NOTES</span></span>

## <span data-ttu-id="e69c1-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="e69c1-149">RELATED LINKS</span></span>

[<span data-ttu-id="e69c1-150">附加 AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="e69c1-150">Add-AzureHDInsightStorage</span></span>](./Add-AzureHDInsightStorage.md)

[<span data-ttu-id="e69c1-151">新-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e69c1-151">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="e69c1-152">新-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="e69c1-152">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)

[<span data-ttu-id="e69c1-153">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="e69c1-153">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)
