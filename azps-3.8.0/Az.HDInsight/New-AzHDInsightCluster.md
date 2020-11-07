---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
ms.openlocfilehash: c0d3d6518025aab22add0859bde69cb1ad279138
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93799201"
---
# <span data-ttu-id="a9d62-101">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="a9d62-101">New-AzHDInsightCluster</span></span>

## <span data-ttu-id="a9d62-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a9d62-102">SYNOPSIS</span></span>
<span data-ttu-id="a9d62-103">在指定的 [資源] 群組中，為目前的訂閱建立 Azure HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="a9d62-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

## <span data-ttu-id="a9d62-104">句法</span><span class="sxs-lookup"><span data-stu-id="a9d62-104">SYNTAX</span></span>

### <span data-ttu-id="a9d62-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="a9d62-105">Default (Default)</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [[-DefaultStorageAccountType] <StorageType>]
 [[-Config] <AzureHDInsightConfig>] [[-OozieMetastore] <AzureHDInsightMetastore>]
 [[-HiveMetastore] <AzureHDInsightMetastore>]
 [[-AdditionalStorageAccounts] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-Configurations] <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [[-ScriptActions] <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [[-DefaultStorageContainer] <String>] [[-DefaultStorageRootPath] <String>] [[-Version] <String>]
 [[-HeadNodeSize] <String>] [[-WorkerNodeSize] <String>] [[-EdgeNodeSize] <String>]
 [[-ZookeeperNodeSize] <String>] [[-ClusterType] <String>]
 [[-ComponentVersion] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-VirtualNetworkId] <String>] [[-SubnetName] <String>] [[-OSType] <OSType>] [[-ClusterTier] <Tier>]
 [[-SshCredential] <PSCredential>] [[-SshPublicKey] <String>] [[-RdpCredential] <PSCredential>]
 [[-RdpAccessExpiry] <DateTime>] [[-ObjectId] <Guid>] [[-ApplicationId] <Guid>]
 [[-CertificatePassword] <String>] [[-AadTenantId] <Guid>] [[-SecurityProfile] <AzureHDInsightSecurityProfile>]
 [[-DisksPerWorkerNode] <Int32>] [[-MinSupportedTlsVersion] <String>]
 [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9d62-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="a9d62-106">CertificateFilePath</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [[-DefaultStorageAccountType] <StorageType>]
 [[-Config] <AzureHDInsightConfig>] [[-OozieMetastore] <AzureHDInsightMetastore>]
 [[-HiveMetastore] <AzureHDInsightMetastore>]
 [[-AdditionalStorageAccounts] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-Configurations] <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [[-ScriptActions] <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [[-DefaultStorageContainer] <String>] [[-DefaultStorageRootPath] <String>] [[-Version] <String>]
 [[-HeadNodeSize] <String>] [[-WorkerNodeSize] <String>] [[-EdgeNodeSize] <String>]
 [[-ZookeeperNodeSize] <String>] [[-ClusterType] <String>]
 [[-ComponentVersion] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-VirtualNetworkId] <String>] [[-SubnetName] <String>] [[-OSType] <OSType>] [[-ClusterTier] <Tier>]
 [[-SshCredential] <PSCredential>] [[-SshPublicKey] <String>] [[-RdpCredential] <PSCredential>]
 [[-RdpAccessExpiry] <DateTime>] [[-ObjectId] <Guid>] [[-ApplicationId] <Guid>]
 [[-CertificateFilePath] <String>] [[-CertificatePassword] <String>] [[-AadTenantId] <Guid>]
 [[-SecurityProfile] <AzureHDInsightSecurityProfile>] [[-DisksPerWorkerNode] <Int32>]
 [[-MinSupportedTlsVersion] <String>] [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9d62-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="a9d62-107">CertificateFileContents</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [[-DefaultStorageAccountType] <StorageType>]
 [[-Config] <AzureHDInsightConfig>] [[-OozieMetastore] <AzureHDInsightMetastore>]
 [[-HiveMetastore] <AzureHDInsightMetastore>]
 [[-AdditionalStorageAccounts] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-Configurations] <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [[-ScriptActions] <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [[-DefaultStorageContainer] <String>] [[-DefaultStorageRootPath] <String>] [[-Version] <String>]
 [[-HeadNodeSize] <String>] [[-WorkerNodeSize] <String>] [[-EdgeNodeSize] <String>]
 [[-ZookeeperNodeSize] <String>] [[-ClusterType] <String>]
 [[-ComponentVersion] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-VirtualNetworkId] <String>] [[-SubnetName] <String>] [[-OSType] <OSType>] [[-ClusterTier] <Tier>]
 [[-SshCredential] <PSCredential>] [[-SshPublicKey] <String>] [[-RdpCredential] <PSCredential>]
 [[-RdpAccessExpiry] <DateTime>] [[-ObjectId] <Guid>] [[-ApplicationId] <Guid>]
 [[-CertificateFileContents] <Byte[]>] [[-CertificatePassword] <String>] [[-AadTenantId] <Guid>]
 [[-SecurityProfile] <AzureHDInsightSecurityProfile>] [[-DisksPerWorkerNode] <Int32>]
 [[-MinSupportedTlsVersion] <String>] [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9d62-108">說明</span><span class="sxs-lookup"><span data-stu-id="a9d62-108">DESCRIPTION</span></span>
<span data-ttu-id="a9d62-109">New-AzHDInsightCluster 會使用指定的參數或使用 New-AzHDInsightClusterConfig Cmdlet 建立的設定物件來建立 Azure HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="a9d62-109">The New-AzHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="a9d62-110">示例</span><span class="sxs-lookup"><span data-stu-id="a9d62-110">EXAMPLES</span></span>

### <span data-ttu-id="a9d62-111">範例1：建立 Azure HDInsight 群集</span><span class="sxs-lookup"><span data-stu-id="a9d62-111">Example 1: Create an Azure HDInsight cluster</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        #   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
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

<span data-ttu-id="a9d62-112">這個命令會在目前的訂閱中建立群集。</span><span class="sxs-lookup"><span data-stu-id="a9d62-112">This command creates a cluster in the current subscription.</span></span>

## <span data-ttu-id="a9d62-113">參數</span><span class="sxs-lookup"><span data-stu-id="a9d62-113">PARAMETERS</span></span>

### <span data-ttu-id="a9d62-114">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="a9d62-114">-AadTenantId</span></span>
<span data-ttu-id="a9d62-115">指定在存取 Azure Data Lake Store 時將使用的 Azure AD 租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="a9d62-115">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d62-116">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="a9d62-116">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="a9d62-117">指定群集的其他 Azure 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="a9d62-117">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="a9d62-118">您也可以使用 Add-AzHDInsightStorage Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a9d62-118">You can alternatively use the Add-AzHDInsightStorage cmdlet.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d62-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="a9d62-119">-ApplicationId</span></span>
<span data-ttu-id="a9d62-120">取得或設定用於存取 Azure Data Lake 的服務主體應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="a9d62-120">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d62-121">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="a9d62-121">-CertificateFileContents</span></span>
<span data-ttu-id="a9d62-122">指定在存取 Azure Data Lake Store 時所要使用的憑證檔案內容。</span><span class="sxs-lookup"><span data-stu-id="a9d62-122">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: CertificateFileContents
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d62-123">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="a9d62-123">-CertificateFilePath</span></span>
<span data-ttu-id="a9d62-124">指定將用來以服務主體進行驗證的憑證檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="a9d62-124">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="a9d62-125">當您存取 Azure Data Lake Store 時，群集會使用此程式。</span><span class="sxs-lookup"><span data-stu-id="a9d62-125">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: CertificateFilePath
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d62-126">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="a9d62-126">-CertificatePassword</span></span>
<span data-ttu-id="a9d62-127">指定將用來驗證為服務主體之憑證的密碼。</span><span class="sxs-lookup"><span data-stu-id="a9d62-127">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="a9d62-128">當您存取 Azure Data Lake Store 時，群集會使用此程式。</span><span class="sxs-lookup"><span data-stu-id="a9d62-128">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d62-129">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a9d62-129">-ClusterName</span></span>
<span data-ttu-id="a9d62-130">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9d62-130">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="a9d62-131">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="a9d62-131">-ClusterSizeInNodes</span></span>
<span data-ttu-id="a9d62-132">指定群集的輔助角色節點數。</span><span class="sxs-lookup"><span data-stu-id="a9d62-132">Specifies the number of Worker nodes for the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d62-133">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="a9d62-133">-ClusterTier</span></span>
<span data-ttu-id="a9d62-134">指定 HDInsight 群集層級。</span><span class="sxs-lookup"><span data-stu-id="a9d62-134">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="a9d62-135">根據預設，這是標準的。</span><span class="sxs-lookup"><span data-stu-id="a9d62-135">By default, this is Standard.</span></span>
<span data-ttu-id="a9d62-136">[特優] 層只能與 Linux 群集搭配使用，並且可讓您使用一些新功能。</span><span class="sxs-lookup"><span data-stu-id="a9d62-136">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

```yaml
Type: Microsoft.Azure.Management.HDInsight.Models.Tier
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d62-137">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="a9d62-137">-ClusterType</span></span>
<span data-ttu-id="a9d62-138">指定要建立的群集類型。</span><span class="sxs-lookup"><span data-stu-id="a9d62-138">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="a9d62-139">選項包括： Hadoop、HBase、風暴、Spark、INTERACTIVEHIVE、Kafka 和 RServer</span><span class="sxs-lookup"><span data-stu-id="a9d62-139">Options are: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka, and RServer</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d62-140">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="a9d62-140">-ComponentVersion</span></span>
```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d62-141">-Config</span><span class="sxs-lookup"><span data-stu-id="a9d62-141">-Config</span></span>
<span data-ttu-id="a9d62-142">指定要用來建立群集的群集物件。</span><span class="sxs-lookup"><span data-stu-id="a9d62-142">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="a9d62-143">您可以使用 New-AzHDInsightClusterConfig Cmdlet 來建立此物件。</span><span class="sxs-lookup"><span data-stu-id="a9d62-143">This object can be created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9d62-144">-配置</span><span class="sxs-lookup"><span data-stu-id="a9d62-144">-Configurations</span></span>
<span data-ttu-id="a9d62-145">指定此 HDInsight 群集的設定。</span><span class="sxs-lookup"><span data-stu-id="a9d62-145">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="a9d62-146">您也可以使用 Add-AzHDInsightConfigValues Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a9d62-146">You can alternatively use the Add-AzHDInsightConfigValues cmdlet.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d62-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9d62-147">-DefaultProfile</span></span>
<span data-ttu-id="a9d62-148">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a9d62-148">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9d62-149">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="a9d62-149">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="a9d62-150">指定 HDInsight 群集將使用的預設 Azure 儲存空間帳戶的帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="a9d62-150">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="a9d62-151">您也可以使用 Set-AzHDInsightDefaultStorage Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a9d62-151">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d62-152">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a9d62-152">-DefaultStorageAccountName</span></span>
<span data-ttu-id="a9d62-153">指定 HDInsight 群集將使用的預設 Azure 儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="a9d62-153">Specifies the name of the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="a9d62-154">您也可以使用 Set-AzHDInsightDefaultStorage Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a9d62-154">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d62-155">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="a9d62-155">-DefaultStorageAccountType</span></span>
<span data-ttu-id="a9d62-156">指定 HDInsight 群集將使用的預設儲存空間類型。</span><span class="sxs-lookup"><span data-stu-id="a9d62-156">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="a9d62-157">可能的值為 AzureStorage 和 AzureDataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="a9d62-157">Possible values are AzureStorage and AzureDataLakeStore.</span></span> <span data-ttu-id="a9d62-158">如果沒有指定，則預設為 AzureStorage。</span><span class="sxs-lookup"><span data-stu-id="a9d62-158">Defaults to AzureStorage if not specified.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: AzureStorage
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d62-159">-DefaultStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a9d62-159">-DefaultStorageContainer</span></span>
<span data-ttu-id="a9d62-160">指定 HDInsight 群集將使用之預設 Azure 儲存空間帳戶中預設容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9d62-160">Specifies the name of the default container in the default Azure storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="a9d62-161">您也可以使用 Set-AzHDInsightDefaultStorage Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a9d62-161">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d62-162">-DefaultStorageRootPath</span><span class="sxs-lookup"><span data-stu-id="a9d62-162">-DefaultStorageRootPath</span></span>
<span data-ttu-id="a9d62-163">指定在 Data Lake Store 帳戶中，HDInsight 群集將用來做為預設 filesystem 的路徑-前置詞。</span><span class="sxs-lookup"><span data-stu-id="a9d62-163">Specifies the path-prefix in the Data Lake Store Account that the HDInsight cluster will use as the default filesystem.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d62-164">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="a9d62-164">-DisksPerWorkerNode</span></span>
<span data-ttu-id="a9d62-165">指定群集中輔助角色節點角色的磁片數。</span><span class="sxs-lookup"><span data-stu-id="a9d62-165">Specifies the number of disks for worker node role in the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d62-166">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="a9d62-166">-EdgeNodeSize</span></span>
<span data-ttu-id="a9d62-167">指定邊緣節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="a9d62-167">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="a9d62-168">使用 Get-AzVMSize 來取得可接受的 VM 大小，並查看 HDInsight 的 [定價] 頁面。</span><span class="sxs-lookup"><span data-stu-id="a9d62-168">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="a9d62-169">這個參數只對 RServer 群集有效。</span><span class="sxs-lookup"><span data-stu-id="a9d62-169">This parameter is valid only for RServer clusters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d62-170">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="a9d62-170">-HeadNodeSize</span></span>
<span data-ttu-id="a9d62-171">指定頭節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="a9d62-171">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="a9d62-172">使用 Get-AzVMSize 來取得可接受的 VM 大小，並查看 HDInsight 的 [定價] 頁面。</span><span class="sxs-lookup"><span data-stu-id="a9d62-172">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d62-173">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="a9d62-173">-HiveMetastore</span></span>
<span data-ttu-id="a9d62-174">指定要儲存 Hive 中繼資料的 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="a9d62-174">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="a9d62-175">您也可以使用 Add-AzHDInsightMetastore Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a9d62-175">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastore
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d62-176">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="a9d62-176">-HttpCredential</span></span>
<span data-ttu-id="a9d62-177">指定群集的群集登入 (HTTP) 認證。</span><span class="sxs-lookup"><span data-stu-id="a9d62-177">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="a9d62-178">-位置</span><span class="sxs-lookup"><span data-stu-id="a9d62-178">-Location</span></span>
<span data-ttu-id="a9d62-179">指定群集的位置。</span><span class="sxs-lookup"><span data-stu-id="a9d62-179">Specifies the location for the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d62-180">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="a9d62-180">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="a9d62-181">取得或設定最低支援的 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="a9d62-181">Gets or sets the minimal supported TLS version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d62-182">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a9d62-182">-ObjectId</span></span>
<span data-ttu-id="a9d62-183">指定 Azure AD 物件識別碼 (代表群集之 Azure AD 服務主體的 GUID) 。</span><span class="sxs-lookup"><span data-stu-id="a9d62-183">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="a9d62-184">當您存取 Azure Data Lake Store 時，群集會使用此程式。</span><span class="sxs-lookup"><span data-stu-id="a9d62-184">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d62-185">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="a9d62-185">-OozieMetastore</span></span>
<span data-ttu-id="a9d62-186">指定 SQL 資料庫以儲存 Oozie 中繼資料。</span><span class="sxs-lookup"><span data-stu-id="a9d62-186">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="a9d62-187">您也可以使用 Add-AzHDInsightMetastore Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a9d62-187">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastore
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d62-188">-OSType</span><span class="sxs-lookup"><span data-stu-id="a9d62-188">-OSType</span></span>
<span data-ttu-id="a9d62-189">指定群集的作業系統。</span><span class="sxs-lookup"><span data-stu-id="a9d62-189">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="a9d62-190">選項包括： Windows、Linux</span><span class="sxs-lookup"><span data-stu-id="a9d62-190">Options are: Windows, Linux</span></span>

```yaml
Type: Microsoft.Azure.Management.HDInsight.Models.OSType
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d62-191">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="a9d62-191">-RdpAccessExpiry</span></span>
<span data-ttu-id="a9d62-192">指定遠端桌面通訊協定的到期日（例如 DateTime 物件） (RDP) 對群集的存取權。</span><span class="sxs-lookup"><span data-stu-id="a9d62-192">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d62-193">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="a9d62-193">-RdpCredential</span></span>
<span data-ttu-id="a9d62-194">為群集指定遠端桌面 (RDP) 認證。</span><span class="sxs-lookup"><span data-stu-id="a9d62-194">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="a9d62-195">這只適用于 Windows 群集。</span><span class="sxs-lookup"><span data-stu-id="a9d62-195">This is only for Windows clusters.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d62-196">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9d62-196">-ResourceGroupName</span></span>
<span data-ttu-id="a9d62-197">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9d62-197">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d62-198">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="a9d62-198">-ScriptActions</span></span>
<span data-ttu-id="a9d62-199">指定在群集建立結束時，要在群集上執行的腳本動作。</span><span class="sxs-lookup"><span data-stu-id="a9d62-199">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="a9d62-200">您也可以使用 [載入 AzHDInsightScriptAction]。</span><span class="sxs-lookup"><span data-stu-id="a9d62-200">You can alternatively use Add-AzHDInsightScriptAction.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]
Parameter Sets: (All)
Aliases:
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d62-201">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="a9d62-201">-SecurityProfile</span></span>
<span data-ttu-id="a9d62-202">指定用來建立安全群集的安全性相關屬性。</span><span class="sxs-lookup"><span data-stu-id="a9d62-202">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="a9d62-203">您也可以使用 Add-AzHDInsightSecurityProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a9d62-203">You can alternatively use the Add-AzHDInsightSecurityProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d62-204">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="a9d62-204">-SshCredential</span></span>
<span data-ttu-id="a9d62-205">指定要用於 SSH 連接的 SSH 認證。</span><span class="sxs-lookup"><span data-stu-id="a9d62-205">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="a9d62-206">這僅適用于 Linux 群集。</span><span class="sxs-lookup"><span data-stu-id="a9d62-206">This is only for Linux clusters.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d62-207">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="a9d62-207">-SshPublicKey</span></span>
<span data-ttu-id="a9d62-208">指定要用於 SSH 連接的公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="a9d62-208">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="a9d62-209">這僅適用于 Linux 群集。</span><span class="sxs-lookup"><span data-stu-id="a9d62-209">This is only for Linux clusters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d62-210">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="a9d62-210">-SubnetName</span></span>
<span data-ttu-id="a9d62-211">在已選取的群集虛擬網路中，指定子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9d62-211">Specifies the name of a subnet within the chosen virtual network for the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d62-212">-版本</span><span class="sxs-lookup"><span data-stu-id="a9d62-212">-Version</span></span>
<span data-ttu-id="a9d62-213">指定 HDInsight 群集的 HDI 版本。</span><span class="sxs-lookup"><span data-stu-id="a9d62-213">Specifies the HDI version of the HDInsight cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d62-214">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="a9d62-214">-VirtualNetworkId</span></span>
<span data-ttu-id="a9d62-215">指定要在其中提供群集的虛擬網路識別碼。</span><span class="sxs-lookup"><span data-stu-id="a9d62-215">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d62-216">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="a9d62-216">-WorkerNodeSize</span></span>
<span data-ttu-id="a9d62-217">指定工作人員節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="a9d62-217">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="a9d62-218">使用 Get-AzVMSize 來取得可接受的 VM 大小，並查看 HDInsight 的 [定價] 頁面。</span><span class="sxs-lookup"><span data-stu-id="a9d62-218">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d62-219">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="a9d62-219">-ZookeeperNodeSize</span></span>
<span data-ttu-id="a9d62-220">指定 Zookeeper 節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="a9d62-220">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="a9d62-221">使用 Get-AzVMSize 來取得可接受的 VM 大小，並查看 HDInsight 的 [定價] 頁面。</span><span class="sxs-lookup"><span data-stu-id="a9d62-221">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="a9d62-222">這個參數只對 HBase 或風暴群集有效。</span><span class="sxs-lookup"><span data-stu-id="a9d62-222">This parameter is valid only for HBase or Storm clusters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d62-223">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9d62-223">CommonParameters</span></span>
<span data-ttu-id="a9d62-224">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a9d62-224">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9d62-225">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a9d62-225">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9d62-226">輸入</span><span class="sxs-lookup"><span data-stu-id="a9d62-226">INPUTS</span></span>

### <span data-ttu-id="a9d62-227">AzureHDInsightConfig （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="a9d62-227">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="a9d62-228">輸出</span><span class="sxs-lookup"><span data-stu-id="a9d62-228">OUTPUTS</span></span>

### <span data-ttu-id="a9d62-229">AzureHDInsightCluster （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="a9d62-229">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="a9d62-230">筆記</span><span class="sxs-lookup"><span data-stu-id="a9d62-230">NOTES</span></span>
<span data-ttu-id="a9d62-231">關鍵字： azure，azurerm，arm，資源，管理，管理員，hadoop，hdinsight，hd，洞察力</span><span class="sxs-lookup"><span data-stu-id="a9d62-231">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="a9d62-232">相關連結</span><span class="sxs-lookup"><span data-stu-id="a9d62-232">RELATED LINKS</span></span>

[<span data-ttu-id="a9d62-233">新-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="a9d62-233">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

