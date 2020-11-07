---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 1B6AC121-1AA0-4D28-B1EA-C96147FDD168
online version: ''
schema: 2.0.0
ms.openlocfilehash: 02435c28ca17666a3b19389fde039353f3d779a0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967162"
---
# <span data-ttu-id="42edf-101">Add-AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="42edf-101">Add-AzureHDInsightStorage</span></span>

## <span data-ttu-id="42edf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="42edf-102">SYNOPSIS</span></span>
<span data-ttu-id="42edf-103">將 blob 儲存空間帳戶專案新增至 HDInsight 配置。</span><span class="sxs-lookup"><span data-stu-id="42edf-103">Adds a blob storage account entry to an HDInsight configuration.</span></span>

## <span data-ttu-id="42edf-104">句法</span><span class="sxs-lookup"><span data-stu-id="42edf-104">SYNTAX</span></span>

```
Add-AzureHDInsightStorage -Config <AzureHDInsightConfig> -StorageAccountKey <String>
 -StorageAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="42edf-105">說明</span><span class="sxs-lookup"><span data-stu-id="42edf-105">DESCRIPTION</span></span>
<span data-ttu-id="42edf-106">此版本的 Azure PowerShell HDInsight 已被否決。</span><span class="sxs-lookup"><span data-stu-id="42edf-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="42edf-107">這些 Cmdlet 將會在2017年1月1日移除。</span><span class="sxs-lookup"><span data-stu-id="42edf-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="42edf-108">請使用較新版本的 Azure PowerShell HDInsight。</span><span class="sxs-lookup"><span data-stu-id="42edf-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="42edf-109">如需如何使用新的 HDInsight 建立群集的相關資訊，請參閱 [使用 Azure PowerShell (在 HDInsight 中建立以 Linux 為基礎的群集](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 。</span><span class="sxs-lookup"><span data-stu-id="42edf-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="42edf-110">如需如何使用 Azure PowerShell 和其他方法提交作業的相關資訊，請參閱 [在 HDInsight 中提交 Hadoop 作業](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) 。</span><span class="sxs-lookup"><span data-stu-id="42edf-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="42edf-111">如需有關 Azure PowerShell HDInsight 的參考資訊，請參閱 [Azure HDInsight Cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="42edf-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="42edf-112">**AzureHDInsightStorage** Cmdlet 會將 [blob 儲存空間] 帳戶專案新增至 Azure HDInsight 配置。</span><span class="sxs-lookup"><span data-stu-id="42edf-112">The **Add-AzureHDInsightStorage** cmdlet adds a blob storage account entry to an Azure HDInsight configuration.</span></span>

## <span data-ttu-id="42edf-113">示例</span><span class="sxs-lookup"><span data-stu-id="42edf-113">EXAMPLES</span></span>

### <span data-ttu-id="42edf-114">範例1：新增儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="42edf-114">Example 1: Add a storage account</span></span>
```
PS C:\>$StoreConfig = Add-AzureHDInsightStorage -Config $Config -StorageAccountName "MyStorage" -StorageAccountKey "Key"
```

<span data-ttu-id="42edf-115">這個命令會將一個名為 MyStorage 的儲存空間帳戶新增至儲存在 $Config 的設定物件，然後將該設定儲存在 $StoreConfig 變數中。</span><span class="sxs-lookup"><span data-stu-id="42edf-115">This command adds a storage account named MyStorage to the configuration object stored in $Config, and then stores the configuration in the $StoreConfig variable.</span></span>

### <span data-ttu-id="42edf-116">範例2：設定多個儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="42edf-116">Example 2: Configure multiple storage accounts</span></span>
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
    | Add-AzureHDInsightMetastore -SqlAzureServerName "Sqlserver01.database.windows.net" -DatabaseName "MyOozieDatabaseName" -Credential $OozieCreds -MetastoreType OozieMetastore 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "Sqlserver01.database.windows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore 
    | New-AzureHDInsightCluster -Subscription $SubID -Credential $Creds
```

<span data-ttu-id="42edf-117">第一個命令使用 **AzureSubscription** Cmdlet 來取得目前的訂閱識別碼，然後將它儲存在 $SubId 變數中。</span><span class="sxs-lookup"><span data-stu-id="42edf-117">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="42edf-118">第二個和第三個命令使用 **AzureStorageKey** Cmdlet 來取得 MyBlobStorage 和 MySecondBlobStorage 的主要儲存空間，然後分別將金鑰儲存在 $Key 1 和 $Key 2 變數中。</span><span class="sxs-lookup"><span data-stu-id="42edf-118">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="42edf-119">第四個、第五個和第六個命令會取得目前訂閱及 Oozie 和 Hive 的認證，然後將認證儲存在變數中。</span><span class="sxs-lookup"><span data-stu-id="42edf-119">The fourth, fifth, and sixth commands get credentials for the current subscription and for Oozie and Hive, and then store the credentials in variables.</span></span>

<span data-ttu-id="42edf-120">最終命令會使用這些 Cmdlet 執行一系列的作業：</span><span class="sxs-lookup"><span data-stu-id="42edf-120">The final command performs a sequence of operations by using these cmdlets:</span></span>

- <span data-ttu-id="42edf-121">建立 HDInsight 群集配置 **的新 AzureHDInsightClusterConfig**</span><span class="sxs-lookup"><span data-stu-id="42edf-121">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration</span></span>
- <span data-ttu-id="42edf-122">**設定-AzureHDInsightDefaultStorage** ，將配置的預設儲存空間帳戶設定為 MyBlobStorage.blob.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="42edf-122">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net</span></span>
- <span data-ttu-id="42edf-123">**AzureHDInsightStorage** 以將名為 MySecondBlobStorage.blob.core.windows.net 的第二個儲存空間帳戶新增至設定</span><span class="sxs-lookup"><span data-stu-id="42edf-123">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration</span></span>
- <span data-ttu-id="42edf-124">**AzureHDInsightStorage** 以將 Oozie 的 Metastore 和 Hive 的 metastore 設定為 configuration</span><span class="sxs-lookup"><span data-stu-id="42edf-124">**Add-AzureHDInsightStorage** to add a metastore for Oozie and a metastore for Hive to the configuration</span></span>
- <span data-ttu-id="42edf-125">使用新的設定建立 HDInsight 群集的 **新 AzureHDInsightCluster**</span><span class="sxs-lookup"><span data-stu-id="42edf-125">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration</span></span>

## <span data-ttu-id="42edf-126">參數</span><span class="sxs-lookup"><span data-stu-id="42edf-126">PARAMETERS</span></span>

### <span data-ttu-id="42edf-127">-Config</span><span class="sxs-lookup"><span data-stu-id="42edf-127">-Config</span></span>
<span data-ttu-id="42edf-128">指定 [配置] 物件。</span><span class="sxs-lookup"><span data-stu-id="42edf-128">Specifies a configuration object.</span></span>
<span data-ttu-id="42edf-129">這個 Cmdlet 會將儲存空間帳戶資訊新增到此參數指定的物件。</span><span class="sxs-lookup"><span data-stu-id="42edf-129">This cmdlet adds storage account information to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="42edf-130">-設定檔</span><span class="sxs-lookup"><span data-stu-id="42edf-130">-Profile</span></span>
<span data-ttu-id="42edf-131">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="42edf-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="42edf-132">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="42edf-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="42edf-133">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="42edf-133">-StorageAccountKey</span></span>
<span data-ttu-id="42edf-134">指定用來存取儲存空間帳戶的儲存空間帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="42edf-134">Specifies the storage account key that is used to access a storage account.</span></span>

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

### <span data-ttu-id="42edf-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="42edf-135">-StorageAccountName</span></span>
<span data-ttu-id="42edf-136">指定要新增之 Azure 儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="42edf-136">Specifies the name of the Azure storage account to add.</span></span>

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

### <span data-ttu-id="42edf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42edf-137">CommonParameters</span></span>
<span data-ttu-id="42edf-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="42edf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42edf-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="42edf-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42edf-140">輸入</span><span class="sxs-lookup"><span data-stu-id="42edf-140">INPUTS</span></span>

## <span data-ttu-id="42edf-141">輸出</span><span class="sxs-lookup"><span data-stu-id="42edf-141">OUTPUTS</span></span>

## <span data-ttu-id="42edf-142">筆記</span><span class="sxs-lookup"><span data-stu-id="42edf-142">NOTES</span></span>

## <span data-ttu-id="42edf-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="42edf-143">RELATED LINKS</span></span>

[<span data-ttu-id="42edf-144">新-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="42edf-144">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="42edf-145">新-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="42edf-145">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)

[<span data-ttu-id="42edf-146">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="42edf-146">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)


