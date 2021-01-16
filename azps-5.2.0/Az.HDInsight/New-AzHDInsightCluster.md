---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
ms.openlocfilehash: f4592a371e528c7779e07251bf79677dac47e6df
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98273315"
---
# <span data-ttu-id="f3c3b-101">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f3c3b-101">New-AzHDInsightCluster</span></span>

## <span data-ttu-id="f3c3b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f3c3b-102">SYNOPSIS</span></span>
<span data-ttu-id="f3c3b-103">在指定的 [資源] 群組中，為目前的訂閱建立 Azure HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

## <span data-ttu-id="f3c3b-104">句法</span><span class="sxs-lookup"><span data-stu-id="f3c3b-104">SYNTAX</span></span>

### <span data-ttu-id="f3c3b-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="f3c3b-105">Default (Default)</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-StorageAccountResourceId] <String>]
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-Config <AzureHDInsightConfig>]
 [-OozieMetastore <AzureHDInsightMetastore>] [-HiveMetastore <AzureHDInsightMetastore>]
 [-AmbariDatabase <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-StorageContainer <String>] [-StorageRootPath <String>] [-StorageFileSystem <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>]
 [-KafkaManagementNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificatePassword <String>]
 [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>] [-DisksPerWorkerNode <Int32>]
 [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>] [-StorageAccountManagedIdentity <String>]
 [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>] [-EncryptionKeyVersion <String>]
 [-EncryptionVaultUri <String>] [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-EnableIDBroker] [-KafkaClientGroupId <String>]
 [-KafkaClientGroupName <String>] [-ResourceProviderConnection <String>] [-PrivateLink <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3c3b-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="f3c3b-106">CertificateFilePath</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-StorageAccountResourceId] <String>]
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-Config <AzureHDInsightConfig>]
 [-OozieMetastore <AzureHDInsightMetastore>] [-HiveMetastore <AzureHDInsightMetastore>]
 [-AmbariDatabase <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-StorageContainer <String>] [-StorageRootPath <String>] [-StorageFileSystem <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>]
 [-KafkaManagementNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>]
 [-StorageAccountManagedIdentity <String>] [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>]
 [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>] [-EncryptionInTransit <Boolean>]
 [-EncryptionAtHost <Boolean>] [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-EnableIDBroker]
 [-KafkaClientGroupId <String>] [-KafkaClientGroupName <String>] [-ResourceProviderConnection <String>]
 [-PrivateLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3c3b-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="f3c3b-107">CertificateFileContents</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-StorageAccountResourceId] <String>]
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-Config <AzureHDInsightConfig>]
 [-OozieMetastore <AzureHDInsightMetastore>] [-HiveMetastore <AzureHDInsightMetastore>]
 [-AmbariDatabase <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-StorageContainer <String>] [-StorageRootPath <String>] [-StorageFileSystem <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>]
 [-KafkaManagementNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFileContents <Byte[]>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>]
 [-StorageAccountManagedIdentity <String>] [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>]
 [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>] [-EncryptionInTransit <Boolean>]
 [-EncryptionAtHost <Boolean>] [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-EnableIDBroker]
 [-KafkaClientGroupId <String>] [-KafkaClientGroupName <String>] [-ResourceProviderConnection <String>]
 [-PrivateLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3c3b-108">說明</span><span class="sxs-lookup"><span data-stu-id="f3c3b-108">DESCRIPTION</span></span>
<span data-ttu-id="f3c3b-109">New-AzHDInsightCluster 會使用指定的參數或使用 New-AzHDInsightClusterConfig Cmdlet 建立的設定物件來建立 Azure HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-109">The New-AzHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="f3c3b-110">示例</span><span class="sxs-lookup"><span data-stu-id="f3c3b-110">EXAMPLES</span></span>

### <span data-ttu-id="f3c3b-111">範例1：建立 Azure HDInsight 群集</span><span class="sxs-lookup"><span data-stu-id="f3c3b-111">Example 1: Create an Azure HDInsight cluster</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
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
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
```

<span data-ttu-id="f3c3b-112">這個命令會在目前的訂閱中建立群集。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-112">This command creates a cluster in the current subscription.</span></span>

### <span data-ttu-id="f3c3b-113">範例2：使用客戶管理的金鑰磁片加密建立群集</span><span class="sxs-lookup"><span data-stu-id="f3c3b-113">Example 2: Create cluster with customer-managed key disk encryption</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-cmk-cluster"
        $clusterCreds = Get-Credential

        # Customer-managed Key info
        $assignedIdentity = "your-ami-resource-id"
        $encryptionKeyName = "new-key"
        $encryptionVaultUri = "https://MyKeyVault.vault.azure.net"
        $encryptionKeyVersion = "00000000000000000000000000000000"

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Spark `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -AssignedIdentity $assignedIdentity `
            -EncryptionKeyName $encryptionKeyName `
            -EncryptionVaultUri $encryptionVaultUri `
            -EncryptionKeyVersion $encryptionKeyVersion
```

### <span data-ttu-id="f3c3b-114">範例3：建立 Azure HDInsight 群集，以便在中轉時加密</span><span class="sxs-lookup"><span data-stu-id="f3c3b-114">Example 3: Create an Azure HDInsight cluster which enables encryption in transit</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
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
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EncryptionInTransit $true `
```

### <span data-ttu-id="f3c3b-115">範例4：使用 [中繼出站] 和 [私人連結] 功能建立 Azure HDInsight 群集</span><span class="sxs-lookup"><span data-stu-id="f3c3b-115">Example 4: Create an Azure HDInsight cluster with relay outbound and private link feature</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
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
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Virtual network info
        $virtualNetworkId="yourvnetresourceid"
        $subnetName="yoursubnetname"

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -VirtualNetworkId $virtualNetworkId -SubnetName $subnetName `
            -ResourceProviderConnection Outbound -PrivateLink Enabled `
```

### <span data-ttu-id="f3c3b-116">範例5：建立 Azure HDInsight 群集，在主機上啟用加密</span><span class="sxs-lookup"><span data-stu-id="f3c3b-116">Example 5: Create an Azure HDInsight cluster which enables encryption at host</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
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
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EncryptionAtHost $true `
```

### <span data-ttu-id="f3c3b-117">範例6：建立可啟用自動縮放的 Azure HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-117">Example 6: Create an Azure HDInsight cluster which enables autoscale.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
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
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create autoscale configuration
        $autoscaleConfiguration=New-AzHDInsightClusterAutoscaleConfiguration `
            -MinWorkerNodeCount 3 -MaxWorkerNodeCount 5

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -AutoscaleConfiguration $autoscaleConfiguration
```

### <span data-ttu-id="f3c3b-118">範例7：使用 Kafka Rest Proxy 建立 Azure HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-118">Example 7: Create an Azure HDInsight cluster with Kafka Rest Proxy.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
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
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Kafka Rest Proxy configuration info
        $kafkaClientGroupName = "yourclientgroupname"
        $kafkaClientGroupId = "yourclientgroupid"
        $kafkaManagementNodeSize = "Standard_D4_v2"
        $disksPerWorkerNode = 2

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Kafka `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -KafkaClientGroupId  $kafkaClientGroupId -KafkaClientGroupName $kafkaClientGroupName `
            -KafkaManagementNodeSize $kafkaManagementNodeSize -DisksPerWorkerNode $disksPerWorkerNode
```

### <span data-ttu-id="f3c3b-119">範例8：建立含 Azure Data Lake Gen2 儲存空間的 Azure HDInsight 群集。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-119">Example 8: Create an Azure HDInsight cluster with Azure Data Lake Gen2 storage.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageManagedIdentity = "yourstorageusermanagedidentity"
        $storageFileSystem = "filesystem01"
        $storageAccountType=AzureDataLakeStorageGen2

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 3 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountManagedIdentity $storageManagedIdentity `
            -StorageFileSystem $storageFileSystem `
            -StorageAccountType $storageAccountType `
            -SshCredential $clusterCreds
```

### <span data-ttu-id="f3c3b-120">範例9：使用企業安全性套件 (ESP) 建立 Azure HDInsight 群集，並啟用 HDInsight ID 代理程式。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-120">Example 9: Create an Azure HDInsight cluster with Enterprise Security Package(ESP) and Enable HDInsight ID Broker.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountKey = "yourstorageaccountaccesskey"
        $storageContainer = "yourcontainer01"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # ESP configuration
        $domainResourceId = "your Azure AD Domin Service resource id"
        $domainUser = "yourdomainuser"
        $domainPassword = "yourdoaminpasswd"
        $domainPassword = ConvertTo-SecureString $domainPassword -AsPlainText -Force
        $domainCredential = New-Object System.Management.Automation.PSCredential($domainUser, $domainPassword)
        $clusterUserGroupDns = "dominusergroup"
        $ldapUrls = "ldaps://{your domain name}:636"

        $clusterTier = Premium
        $vnetId = "yourvnetid"
        $subnetName = "yoursubnetname"
        $assignedIdentity = "your user managed assigned identity resourcee id"

        #Create security profile
        $config= New-AzHDInsightClusterConfig|Add-AzHDInsightSecurityProfile -DomainResourceId $domainResourceId -DomainUserCredential $domainCredential -LdapsUrls $ldapUrls -ClusterUsersGroupDNs $clusterUserGroupDns

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusteTier $clusterTier `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 3 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -VirtualNetworkId $vnetId -SubnetName $subnetName `
            -AssignedIdentity $assignedIdentity `
            -SecurityProfile $config.SecurityProfile -EnableIDBroker
```

## <span data-ttu-id="f3c3b-121">參數</span><span class="sxs-lookup"><span data-stu-id="f3c3b-121">PARAMETERS</span></span>

### <span data-ttu-id="f3c3b-122">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="f3c3b-122">-AadTenantId</span></span>
<span data-ttu-id="f3c3b-123">指定在存取 Azure Data Lake Store 時將使用的 Azure AD 租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-123">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="f3c3b-124">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="f3c3b-124">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="f3c3b-125">指定群集的其他 Azure 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-125">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="f3c3b-126">您也可以使用 Add-AzHDInsightStorage Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-126">You can alternatively use the Add-AzHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="f3c3b-127">-AmbariDatabase</span><span class="sxs-lookup"><span data-stu-id="f3c3b-127">-AmbariDatabase</span></span>
<span data-ttu-id="f3c3b-128">取得或設定 ambari 的資料庫。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-128">Gets or sets the database for ambari.</span></span>

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

### <span data-ttu-id="f3c3b-129">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="f3c3b-129">-ApplicationId</span></span>
<span data-ttu-id="f3c3b-130">取得或設定用於存取 Azure Data Lake 的服務主體應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-130">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="f3c3b-131">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="f3c3b-131">-AssignedIdentity</span></span>
<span data-ttu-id="f3c3b-132">取得或設定指派的身分識別。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-132">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="f3c3b-133">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3c3b-133">-AutoscaleConfiguration</span></span>
<span data-ttu-id="f3c3b-134">取得或設定自動縮放設定</span><span class="sxs-lookup"><span data-stu-id="f3c3b-134">Gets or sets the autoscale configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c3b-135">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="f3c3b-135">-CertificateFileContents</span></span>
<span data-ttu-id="f3c3b-136">指定在存取 Azure Data Lake Store 時所要使用的憑證檔案內容。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-136">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="f3c3b-137">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="f3c3b-137">-CertificateFilePath</span></span>
<span data-ttu-id="f3c3b-138">指定將用來以服務主體進行驗證的憑證檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-138">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="f3c3b-139">當您存取 Azure Data Lake Store 時，群集會使用此程式。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-139">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="f3c3b-140">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="f3c3b-140">-CertificatePassword</span></span>
<span data-ttu-id="f3c3b-141">指定將用來驗證為服務主體之憑證的密碼。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-141">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="f3c3b-142">當您存取 Azure Data Lake Store 時，群集會使用此程式。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-142">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="f3c3b-143">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f3c3b-143">-ClusterName</span></span>
<span data-ttu-id="f3c3b-144">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-144">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="f3c3b-145">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="f3c3b-145">-ClusterSizeInNodes</span></span>
<span data-ttu-id="f3c3b-146">指定群集的輔助角色節點數。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-146">Specifies the number of Worker nodes for the cluster.</span></span>

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

### <span data-ttu-id="f3c3b-147">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="f3c3b-147">-ClusterTier</span></span>
<span data-ttu-id="f3c3b-148">指定 HDInsight 群集層級。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-148">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="f3c3b-149">根據預設，這是標準的。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-149">By default, this is Standard.</span></span>
<span data-ttu-id="f3c3b-150">[特優] 層只能與 Linux 群集搭配使用，並且可讓您使用一些新功能。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-150">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="f3c3b-151">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="f3c3b-151">-ClusterType</span></span>
<span data-ttu-id="f3c3b-152">指定要建立的群集類型。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-152">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="f3c3b-153">選項包括： Hadoop、HBase、風暴、Spark、INTERACTIVEHIVE、Kafka 和 RServer</span><span class="sxs-lookup"><span data-stu-id="f3c3b-153">Options are: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka, and RServer</span></span>

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

### <span data-ttu-id="f3c3b-154">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="f3c3b-154">-ComponentVersion</span></span>
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

### <span data-ttu-id="f3c3b-155">-Config</span><span class="sxs-lookup"><span data-stu-id="f3c3b-155">-Config</span></span>
<span data-ttu-id="f3c3b-156">指定要用來建立群集的群集物件。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-156">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="f3c3b-157">您可以使用 New-AzHDInsightClusterConfig Cmdlet 來建立此物件。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-157">This object can be created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="f3c3b-158">-配置</span><span class="sxs-lookup"><span data-stu-id="f3c3b-158">-Configurations</span></span>
<span data-ttu-id="f3c3b-159">指定此 HDInsight 群集的設定。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-159">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="f3c3b-160">您也可以使用 Add-AzHDInsightConfigValues Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-160">You can alternatively use the Add-AzHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="f3c3b-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3c3b-161">-DefaultProfile</span></span>
<span data-ttu-id="f3c3b-162">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f3c3b-162">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3c3b-163">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="f3c3b-163">-DisksPerWorkerNode</span></span>
<span data-ttu-id="f3c3b-164">指定群集中輔助角色節點角色的磁片數。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-164">Specifies the number of disks for worker node role in the cluster.</span></span>

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

### <span data-ttu-id="f3c3b-165">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="f3c3b-165">-EdgeNodeSize</span></span>
<span data-ttu-id="f3c3b-166">指定邊緣節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-166">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="f3c3b-167">使用 Get-AzVMSize 來取得可接受的 VM 大小，並查看 HDInsight 的 [定價] 頁面。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-167">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="f3c3b-168">這個參數只對 RServer 群集有效。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-168">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="f3c3b-169">-EnableIDBroker</span><span class="sxs-lookup"><span data-stu-id="f3c3b-169">-EnableIDBroker</span></span>
<span data-ttu-id="f3c3b-170">啟用 HDInsight 身分識別代理程式功能。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-170">Enables HDInsight Identity Broker feature.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c3b-171">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="f3c3b-171">-EncryptionAlgorithm</span></span>
<span data-ttu-id="f3c3b-172">取得或設定加密演算法。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-172">Gets or sets the encryption algorithm.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA-OAEP, RSA-OAEP-256, RSA1_5

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c3b-173">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="f3c3b-173">-EncryptionAtHost</span></span>
<span data-ttu-id="f3c3b-174">取得或設定標誌，以指出是否要在主機上啟用加密。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-174">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c3b-175">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="f3c3b-175">-EncryptionInTransit</span></span>
<span data-ttu-id="f3c3b-176">取得或設定標誌，以指出是否要在傳輸中啟用加密。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-176">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c3b-177">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="f3c3b-177">-EncryptionKeyName</span></span>
<span data-ttu-id="f3c3b-178">取得或設定加密金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-178">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="f3c3b-179">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="f3c3b-179">-EncryptionKeyVersion</span></span>
<span data-ttu-id="f3c3b-180">取得或設定加密金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-180">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="f3c3b-181">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="f3c3b-181">-EncryptionVaultUri</span></span>
<span data-ttu-id="f3c3b-182">取得或設定加密 vault uri。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-182">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="f3c3b-183">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="f3c3b-183">-HeadNodeSize</span></span>
<span data-ttu-id="f3c3b-184">指定頭節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-184">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="f3c3b-185">使用 Get-AzVMSize 來取得可接受的 VM 大小，並查看 HDInsight 的 [定價] 頁面。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-185">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="f3c3b-186">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="f3c3b-186">-HiveMetastore</span></span>
<span data-ttu-id="f3c3b-187">指定要儲存 Hive 中繼資料的 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-187">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="f3c3b-188">您也可以使用 Add-AzHDInsightMetastore Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-188">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="f3c3b-189">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="f3c3b-189">-HttpCredential</span></span>
<span data-ttu-id="f3c3b-190">指定群集的群集登入 (HTTP) 認證。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-190">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="f3c3b-191">-KafkaClientGroupId</span><span class="sxs-lookup"><span data-stu-id="f3c3b-191">-KafkaClientGroupId</span></span>
<span data-ttu-id="f3c3b-192">取得或設定 Kafka Rest Proxy 存取的用戶端群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-192">Gets or sets the client group id for Kafka Rest Proxy access.</span></span>

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

### <span data-ttu-id="f3c3b-193">-KafkaClientGroupName</span><span class="sxs-lookup"><span data-stu-id="f3c3b-193">-KafkaClientGroupName</span></span>
<span data-ttu-id="f3c3b-194">取得或設定 Kafka Rest Proxy 存取的用戶端組名。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-194">Gets or sets the client group name for Kafka Rest Proxy access.</span></span>

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

### <span data-ttu-id="f3c3b-195">-KafkaManagementNodeSize</span><span class="sxs-lookup"><span data-stu-id="f3c3b-195">-KafkaManagementNodeSize</span></span>
<span data-ttu-id="f3c3b-196">取得或設定 Kafka 管理節點的大小。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-196">Gets or sets the size of the Kafka Management Node.</span></span>

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

### <span data-ttu-id="f3c3b-197">-位置</span><span class="sxs-lookup"><span data-stu-id="f3c3b-197">-Location</span></span>
<span data-ttu-id="f3c3b-198">指定群集的位置。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-198">Specifies the location for the cluster.</span></span>

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

### <span data-ttu-id="f3c3b-199">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="f3c3b-199">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="f3c3b-200">取得或設定最低支援的 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-200">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="f3c3b-201">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f3c3b-201">-ObjectId</span></span>
<span data-ttu-id="f3c3b-202">指定 Azure AD 物件識別碼 (代表群集之 Azure AD 服務主體的 GUID) 。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-202">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="f3c3b-203">當您存取 Azure Data Lake Store 時，群集會使用此程式。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-203">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="f3c3b-204">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="f3c3b-204">-OozieMetastore</span></span>
<span data-ttu-id="f3c3b-205">指定 SQL 資料庫以儲存 Oozie 中繼資料。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-205">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="f3c3b-206">您也可以使用 Add-AzHDInsightMetastore Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-206">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="f3c3b-207">-OSType</span><span class="sxs-lookup"><span data-stu-id="f3c3b-207">-OSType</span></span>
<span data-ttu-id="f3c3b-208">指定群集的作業系統。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-208">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="f3c3b-209">選項包括： Windows、Linux</span><span class="sxs-lookup"><span data-stu-id="f3c3b-209">Options are: Windows, Linux</span></span>

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

### <span data-ttu-id="f3c3b-210">-PrivateLink</span><span class="sxs-lookup"><span data-stu-id="f3c3b-210">-PrivateLink</span></span>
<span data-ttu-id="f3c3b-211">取得或設定私人連結類型。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-211">Gets or sets the private link type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c3b-212">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="f3c3b-212">-RdpAccessExpiry</span></span>
<span data-ttu-id="f3c3b-213">指定遠端桌面通訊協定的到期日（例如 DateTime 物件） (RDP) 對群集的存取權。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-213">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

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

### <span data-ttu-id="f3c3b-214">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="f3c3b-214">-RdpCredential</span></span>
<span data-ttu-id="f3c3b-215">為群集指定遠端桌面 (RDP) 認證。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-215">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="f3c3b-216">這只適用于 Windows 群集。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-216">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="f3c3b-217">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3c3b-217">-ResourceGroupName</span></span>
<span data-ttu-id="f3c3b-218">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-218">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f3c3b-219">-ResourceProviderConnection</span><span class="sxs-lookup"><span data-stu-id="f3c3b-219">-ResourceProviderConnection</span></span>
<span data-ttu-id="f3c3b-220">取得或設定資源提供者連線類型。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-220">Gets or sets the resource provider connection type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Inbound, Outbound

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c3b-221">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="f3c3b-221">-ScriptActions</span></span>
<span data-ttu-id="f3c3b-222">指定在群集建立結束時，要在群集上執行的腳本動作。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-222">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="f3c3b-223">您也可以使用 [載入 AzHDInsightScriptAction]。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-223">You can alternatively use Add-AzHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="f3c3b-224">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="f3c3b-224">-SecurityProfile</span></span>
<span data-ttu-id="f3c3b-225">指定用來建立安全群集的安全性相關屬性。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-225">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="f3c3b-226">您也可以使用 Add-AzHDInsightSecurityProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-226">You can alternatively use the Add-AzHDInsightSecurityProfile cmdlet.</span></span>

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

### <span data-ttu-id="f3c3b-227">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="f3c3b-227">-SshCredential</span></span>
<span data-ttu-id="f3c3b-228">指定要用於 SSH 連接的 SSH 認證。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-228">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="f3c3b-229">這僅適用于 Linux 群集。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-229">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="f3c3b-230">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="f3c3b-230">-SshPublicKey</span></span>
<span data-ttu-id="f3c3b-231">指定要用於 SSH 連接的公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-231">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="f3c3b-232">這僅適用于 Linux 群集。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-232">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="f3c3b-233">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="f3c3b-233">-StorageAccountKey</span></span>
<span data-ttu-id="f3c3b-234">取得或設定儲存空間帳戶的儲存空間帳戶存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-234">Gets or sets the Storage Account Access Key for the Storage Account.</span></span>

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

### <span data-ttu-id="f3c3b-235">-StorageAccountManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="f3c3b-235">-StorageAccountManagedIdentity</span></span>
<span data-ttu-id="f3c3b-236">取得或設定儲存帳戶管理的身分識別。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-236">Gets or sets the storage account managed identity.</span></span>

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

### <span data-ttu-id="f3c3b-237">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="f3c3b-237">-StorageAccountResourceId</span></span>
<span data-ttu-id="f3c3b-238">取得或設定儲存空間帳戶的儲存資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-238">Gets or sets the Storage Resource Id for the Storage Account.</span></span>

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

### <span data-ttu-id="f3c3b-239">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="f3c3b-239">-StorageAccountType</span></span>
<span data-ttu-id="f3c3b-240">取得或設定儲存空間帳戶的類型。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-240">Gets or sets the type of the storage account.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore, AzureDataLakeStorageGen2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c3b-241">-StorageContainer</span><span class="sxs-lookup"><span data-stu-id="f3c3b-241">-StorageContainer</span></span>
<span data-ttu-id="f3c3b-242">取得或設定預設 Azure 儲存空間帳戶的 StorageContainer 名稱</span><span class="sxs-lookup"><span data-stu-id="f3c3b-242">Gets or sets the StorageContainer name for the default Azure Storage Account</span></span>

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

### <span data-ttu-id="f3c3b-243">-StorageFileSystem</span><span class="sxs-lookup"><span data-stu-id="f3c3b-243">-StorageFileSystem</span></span>
<span data-ttu-id="f3c3b-244">取得或設定預設 Azure Data Lake Storage Gen2 帳戶的檔案系統。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-244">Gets or sets the file system for the default Azure Data Lake Storage Gen2 account.</span></span>

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

### <span data-ttu-id="f3c3b-245">-StorageRootPath</span><span class="sxs-lookup"><span data-stu-id="f3c3b-245">-StorageRootPath</span></span>
<span data-ttu-id="f3c3b-246">取得或設定預設資料 Lake Store 帳戶中群集根目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-246">Gets or sets the path to the root of the cluster in the default Data Lake Store Account.</span></span>

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

### <span data-ttu-id="f3c3b-247">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="f3c3b-247">-SubnetName</span></span>
<span data-ttu-id="f3c3b-248">取得或設定此 HDInsight 群集的子網名稱。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-248">Gets or sets the subnet name for this HDInsight cluster.</span></span>

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

### <span data-ttu-id="f3c3b-249">-版本</span><span class="sxs-lookup"><span data-stu-id="f3c3b-249">-Version</span></span>
<span data-ttu-id="f3c3b-250">指定 HDInsight 群集的 HDI 版本。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-250">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="f3c3b-251">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="f3c3b-251">-VirtualNetworkId</span></span>
<span data-ttu-id="f3c3b-252">指定要在其中提供群集的虛擬網路識別碼。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-252">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="f3c3b-253">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="f3c3b-253">-WorkerNodeSize</span></span>
<span data-ttu-id="f3c3b-254">指定工作人員節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-254">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="f3c3b-255">使用 Get-AzVMSize 來取得可接受的 VM 大小，並查看 HDInsight 的 [定價] 頁面。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-255">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="f3c3b-256">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="f3c3b-256">-ZookeeperNodeSize</span></span>
<span data-ttu-id="f3c3b-257">指定 Zookeeper 節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-257">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="f3c3b-258">使用 Get-AzVMSize 來取得可接受的 VM 大小，並查看 HDInsight 的 [定價] 頁面。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-258">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="f3c3b-259">這個參數只對 HBase 或風暴群集有效。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-259">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="f3c3b-260">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3c3b-260">CommonParameters</span></span>
<span data-ttu-id="f3c3b-261">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-261">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3c3b-262">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-262">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3c3b-263">輸入</span><span class="sxs-lookup"><span data-stu-id="f3c3b-263">INPUTS</span></span>

### <span data-ttu-id="f3c3b-264">AzureHDInsightConfig （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-264">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="f3c3b-265">輸出</span><span class="sxs-lookup"><span data-stu-id="f3c3b-265">OUTPUTS</span></span>

### <span data-ttu-id="f3c3b-266">AzureHDInsightCluster （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="f3c3b-266">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="f3c3b-267">筆記</span><span class="sxs-lookup"><span data-stu-id="f3c3b-267">NOTES</span></span>
<span data-ttu-id="f3c3b-268">關鍵字： azure，azurerm，arm，資源，管理，管理員，hadoop，hdinsight，hd，洞察力</span><span class="sxs-lookup"><span data-stu-id="f3c3b-268">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="f3c3b-269">相關連結</span><span class="sxs-lookup"><span data-stu-id="f3c3b-269">RELATED LINKS</span></span>

[<span data-ttu-id="f3c3b-270">新-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="f3c3b-270">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

