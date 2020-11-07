---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: FF41DDBA-6D4B-47A5-BCFF-3D0BB1D375C5
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2b6aaf5e8564b3eea675a57176b8f7118d2c7a1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967406"
---
# <span data-ttu-id="c0b4a-101">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="c0b4a-101">Set-AzureHDInsightDefaultStorage</span></span>

## <span data-ttu-id="c0b4a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c0b4a-102">SYNOPSIS</span></span>
<span data-ttu-id="c0b4a-103">設定 HDInsight 群集的預設儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="c0b4a-103">Sets the default storage account for an HDInsight cluster.</span></span>

## <span data-ttu-id="c0b4a-104">句法</span><span class="sxs-lookup"><span data-stu-id="c0b4a-104">SYNTAX</span></span>

```
Set-AzureHDInsightDefaultStorage -Config <AzureHDInsightConfig> -StorageAccountKey <String>
 -StorageAccountName <String> -StorageContainerName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c0b4a-105">說明</span><span class="sxs-lookup"><span data-stu-id="c0b4a-105">DESCRIPTION</span></span>
<span data-ttu-id="c0b4a-106">此版本的 Azure PowerShell HDInsight 已被否決。</span><span class="sxs-lookup"><span data-stu-id="c0b4a-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="c0b4a-107">這些 Cmdlet 將會在2017年1月1日移除。</span><span class="sxs-lookup"><span data-stu-id="c0b4a-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="c0b4a-108">請使用較新版本的 Azure PowerShell HDInsight。</span><span class="sxs-lookup"><span data-stu-id="c0b4a-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="c0b4a-109">如需如何使用新的 HDInsight 建立群集的相關資訊，請參閱 [使用 Azure PowerShell (在 HDInsight 中建立以 Linux 為基礎的群集](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 。</span><span class="sxs-lookup"><span data-stu-id="c0b4a-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="c0b4a-110">如需如何使用 Azure PowerShell 和其他方法提交作業的相關資訊，請參閱 [在 HDInsight 中提交 Hadoop 作業](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) 。</span><span class="sxs-lookup"><span data-stu-id="c0b4a-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="c0b4a-111">如需有關 Azure PowerShell HDInsight 的參考資訊，請參閱 [Azure HDInsight Cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="c0b4a-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="c0b4a-112">**AzureHDInsightDefaultStorage** Cmdlet 會設定 HDInsight 群集配置的預設儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="c0b4a-112">The **Set-AzureHDInsightDefaultStorage** cmdlet sets the default storage account for an HDInsight cluster configuration.</span></span>

## <span data-ttu-id="c0b4a-113">示例</span><span class="sxs-lookup"><span data-stu-id="c0b4a-113">EXAMPLES</span></span>

### <span data-ttu-id="c0b4a-114">範例1：設定預設儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="c0b4a-114">Example 1: Set the default storage account</span></span>
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

<span data-ttu-id="c0b4a-115">第一個命令使用 **AzureSubscription** Cmdlet 來取得目前的訂閱識別碼，然後將它儲存在 $SubId 變數中。</span><span class="sxs-lookup"><span data-stu-id="c0b4a-115">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="c0b4a-116">第二個和第三個命令使用 **AzureStorageKey** Cmdlet 來取得 MyBlobStorage 和 MySecondBlobStorage 的主要儲存空間，然後分別將金鑰儲存在 $Key 1 和 $Key 2 變數中。</span><span class="sxs-lookup"><span data-stu-id="c0b4a-116">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="c0b4a-117">第四個、第五個和第六個命令使用 **取得認證** Cmdlet 來取得目前訂閱的認證，然後將認證儲存在 $Creds、$OozieCreds 及 $HiveCreds 變數中。</span><span class="sxs-lookup"><span data-stu-id="c0b4a-117">The fourth, fifth, and sixth commands use the **Get-Credential** cmdlet to get credentials for the current subscription, and then stores the credentials in the $Creds, $OozieCreds, and $HiveCreds variables.</span></span>

<span data-ttu-id="c0b4a-118">最終命令會使用這些 Cmdlet 執行一系列的作業：</span><span class="sxs-lookup"><span data-stu-id="c0b4a-118">The final command performs a sequence of operations by using these cmdlets:</span></span> 

- <span data-ttu-id="c0b4a-119">[ **新增-AzureHDInsightClusterConfig** ] 可建立 HDInsight 群集設定。</span><span class="sxs-lookup"><span data-stu-id="c0b4a-119">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration.</span></span>
- <span data-ttu-id="c0b4a-120">**設定-AzureHDInsightDefaultStorage** ，將配置的預設儲存空間帳戶設定為 MyBlobStorage.blob.core.windows.net。</span><span class="sxs-lookup"><span data-stu-id="c0b4a-120">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net.</span></span>
- <span data-ttu-id="c0b4a-121">[ **載入 AzureHDInsightStorage** ]，將名為 MySecondBlobStorage.blob.core.windows.net 的第二個儲存空間帳戶新增至設定。</span><span class="sxs-lookup"><span data-stu-id="c0b4a-121">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration.</span></span>
- <span data-ttu-id="c0b4a-122">[ **AzureHDInsightMetastore** ]，將 Oozie 的 Metastore 和 Hive 的 metastore 設定為 [配置]。</span><span class="sxs-lookup"><span data-stu-id="c0b4a-122">**Add-AzureHDInsightMetastore** to add a metastore for Oozie and a metastore for Hive to the configuration.</span></span>
- <span data-ttu-id="c0b4a-123">[ **新增-AzureHDInsightCluster** ] 以使用新的設定建立 HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="c0b4a-123">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration.</span></span>

## <span data-ttu-id="c0b4a-124">參數</span><span class="sxs-lookup"><span data-stu-id="c0b4a-124">PARAMETERS</span></span>

### <span data-ttu-id="c0b4a-125">-Config</span><span class="sxs-lookup"><span data-stu-id="c0b4a-125">-Config</span></span>
<span data-ttu-id="c0b4a-126">指定 [配置] 物件。</span><span class="sxs-lookup"><span data-stu-id="c0b4a-126">Specifies a configuration object.</span></span>
<span data-ttu-id="c0b4a-127">這個 Cmdlet 會針對此參數指定的物件設定預設儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="c0b4a-127">This cmdlet sets the default storage account for the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="c0b4a-128">-設定檔</span><span class="sxs-lookup"><span data-stu-id="c0b4a-128">-Profile</span></span>
<span data-ttu-id="c0b4a-129">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="c0b4a-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c0b4a-130">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="c0b4a-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c0b4a-131">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="c0b4a-131">-StorageAccountKey</span></span>
<span data-ttu-id="c0b4a-132">指定用來存取預設儲存空間帳戶的儲存空間帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="c0b4a-132">Specifies the storage account key that is used to access the default storage account.</span></span>

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

### <span data-ttu-id="c0b4a-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c0b4a-133">-StorageAccountName</span></span>
<span data-ttu-id="c0b4a-134">指定預設儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="c0b4a-134">Specifies the name of a default storage account.</span></span>

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

### <span data-ttu-id="c0b4a-135">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="c0b4a-135">-StorageContainerName</span></span>
<span data-ttu-id="c0b4a-136">指定群集預設儲存容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="c0b4a-136">Specifies the name of the default storage container for a cluster.</span></span>

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

### <span data-ttu-id="c0b4a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0b4a-137">CommonParameters</span></span>
<span data-ttu-id="c0b4a-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c0b4a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0b4a-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c0b4a-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0b4a-140">輸入</span><span class="sxs-lookup"><span data-stu-id="c0b4a-140">INPUTS</span></span>

## <span data-ttu-id="c0b4a-141">輸出</span><span class="sxs-lookup"><span data-stu-id="c0b4a-141">OUTPUTS</span></span>

## <span data-ttu-id="c0b4a-142">筆記</span><span class="sxs-lookup"><span data-stu-id="c0b4a-142">NOTES</span></span>

## <span data-ttu-id="c0b4a-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="c0b4a-143">RELATED LINKS</span></span>

[<span data-ttu-id="c0b4a-144">附加 AzureHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="c0b4a-144">Add-AzureHDInsightMetastore</span></span>](./Add-AzureHDInsightMetastore.md)

[<span data-ttu-id="c0b4a-145">附加 AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="c0b4a-145">Add-AzureHDInsightStorage</span></span>](./Add-AzureHDInsightStorage.md)

[<span data-ttu-id="c0b4a-146">新-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c0b4a-146">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="c0b4a-147">新-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="c0b4a-147">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)


