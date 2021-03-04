---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/new-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
ms.openlocfilehash: 94b982eb2add8341b861732bef5e63d88e67a937
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916558"
---
# <span data-ttu-id="cbd27-101">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="cbd27-101">New-AzHDInsightCluster</span></span>

## <span data-ttu-id="cbd27-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cbd27-102">SYNOPSIS</span></span>
<span data-ttu-id="cbd27-103">在目前訂閱的指定資源群組中建立 Azure HDInsight 群組。</span><span class="sxs-lookup"><span data-stu-id="cbd27-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

## <span data-ttu-id="cbd27-104">語法</span><span class="sxs-lookup"><span data-stu-id="cbd27-104">SYNTAX</span></span>

### <span data-ttu-id="cbd27-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="cbd27-105">Default (Default)</span></span>
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
 [-EnableComputeIsolation] [-ComputeIsolationHostSku <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cbd27-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="cbd27-106">CertificateFilePath</span></span>
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
 [-PrivateLink <String>] [-EnableComputeIsolation] [-ComputeIsolationHostSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cbd27-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="cbd27-107">CertificateFileContents</span></span>
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
 [-PrivateLink <String>] [-EnableComputeIsolation] [-ComputeIsolationHostSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbd27-108">描述</span><span class="sxs-lookup"><span data-stu-id="cbd27-108">DESCRIPTION</span></span>
<span data-ttu-id="cbd27-109">此New-AzHDInsightCluster會使用指定的參數，或是使用使用 New-AzHDInsightClusterConfig Cmdlet 所建立設定物件來建立 Azure HDInsight 集區。</span><span class="sxs-lookup"><span data-stu-id="cbd27-109">The New-AzHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="cbd27-110">例子</span><span class="sxs-lookup"><span data-stu-id="cbd27-110">EXAMPLES</span></span>

### <span data-ttu-id="cbd27-111">範例 1：建立 Azure HDInsight 集區</span><span class="sxs-lookup"><span data-stu-id="cbd27-111">Example 1: Create an Azure HDInsight cluster</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
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

<span data-ttu-id="cbd27-112">此命令會建立目前訂閱中的一個集區。</span><span class="sxs-lookup"><span data-stu-id="cbd27-112">This command creates a cluster in the current subscription.</span></span>

### <span data-ttu-id="cbd27-113">範例 2：使用客戶管理的金鑰磁片加密建立組</span><span class="sxs-lookup"><span data-stu-id="cbd27-113">Example 2: Create cluster with customer-managed key disk encryption</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
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

### <span data-ttu-id="cbd27-114">範例 3：建立 Azure HDInsight 集區，啟用傳輸加密</span><span class="sxs-lookup"><span data-stu-id="cbd27-114">Example 3: Create an Azure HDInsight cluster which enables encryption in transit</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}}
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

### <span data-ttu-id="cbd27-115">範例 4：使用轉場外連和私人連結功能建立 Azure HDInsight 集區</span><span class="sxs-lookup"><span data-stu-id="cbd27-115">Example 4: Create an Azure HDInsight cluster with relay outbound and private link feature</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
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

### <span data-ttu-id="cbd27-116">範例 5：建立 Azure HDInsight 集區，啟用主機加密</span><span class="sxs-lookup"><span data-stu-id="cbd27-116">Example 5: Create an Azure HDInsight cluster which enables encryption at host</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
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

### <span data-ttu-id="cbd27-117">範例 6：建立啟用自動縮放的 Azure HDInsight 集區。</span><span class="sxs-lookup"><span data-stu-id="cbd27-117">Example 6: Create an Azure HDInsight cluster which enables autoscale.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
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

### <span data-ttu-id="cbd27-118">範例 7：使用 Kafka Rest Proxy 建立 Azure HDInsight 集區。</span><span class="sxs-lookup"><span data-stu-id="cbd27-118">Example 7: Create an Azure HDInsight cluster with Kafka Rest Proxy.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
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

### <span data-ttu-id="cbd27-119">範例 8：使用 Azure Data Lake Gen2 儲存空間建立 Azure HDInsight 集區。</span><span class="sxs-lookup"><span data-stu-id="cbd27-119">Example 8: Create an Azure HDInsight cluster with Azure Data Lake Gen2 storage.</span></span>
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

### <span data-ttu-id="cbd27-120">範例 9：使用企業安全性套件建立 Azure HDInsight (ESP) 及啟用 HDInsight ID 一文集。</span><span class="sxs-lookup"><span data-stu-id="cbd27-120">Example 9: Create an Azure HDInsight cluster with Enterprise Security Package(ESP) and Enable HDInsight ID Broker.</span></span>
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

### <span data-ttu-id="cbd27-121">範例 10：建立啟用計算隔離的 Azure HDInsight 集區。</span><span class="sxs-lookup"><span data-stu-id="cbd27-121">Example 10: Create an Azure HDInsight cluster which enables compute isolation.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential
        $workerNodeSize="Standard_E16S_V3" # here is just an example
        $headNodeSize="Standard_E8S_V3"
        $zookeeperNodeSize="Standard_E2S_V3"

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -WorkerNodeSize $workerNodeSize `
            -HeadNodeSize $headNodeSize `
            -ZookeeperNodeSize $zookeeperNodeSize `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EnableComputeIsolation `
```

## <span data-ttu-id="cbd27-122">參數</span><span class="sxs-lookup"><span data-stu-id="cbd27-122">PARAMETERS</span></span>

### <span data-ttu-id="cbd27-123">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="cbd27-123">-AadTenantId</span></span>
<span data-ttu-id="cbd27-124">指定存取 Azure Data Lake Store 時將會使用的 Azure AD 租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="cbd27-124">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="cbd27-125">-其他StorageAccount</span><span class="sxs-lookup"><span data-stu-id="cbd27-125">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="cbd27-126">指定該組組的其他 Azure 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="cbd27-126">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="cbd27-127">您也可以使用 Add-AzHDInsightStorage Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cbd27-127">You can alternatively use the Add-AzHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="cbd27-128">-AmbariDatabase</span><span class="sxs-lookup"><span data-stu-id="cbd27-128">-AmbariDatabase</span></span>
<span data-ttu-id="cbd27-129">為 ambari 獲取或設定資料庫。</span><span class="sxs-lookup"><span data-stu-id="cbd27-129">Gets or sets the database for ambari.</span></span>

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

### <span data-ttu-id="cbd27-130">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="cbd27-130">-ApplicationId</span></span>
<span data-ttu-id="cbd27-131">取得或設定存取 Azure Data Lake 的服務主體應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="cbd27-131">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="cbd27-132">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="cbd27-132">-AssignedIdentity</span></span>
<span data-ttu-id="cbd27-133">獲取或設定指派的身分識別。</span><span class="sxs-lookup"><span data-stu-id="cbd27-133">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="cbd27-134">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="cbd27-134">-AutoscaleConfiguration</span></span>
<span data-ttu-id="cbd27-135">獲取或設定自動縮放設定</span><span class="sxs-lookup"><span data-stu-id="cbd27-135">Gets or sets the autoscale configuration</span></span>

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

### <span data-ttu-id="cbd27-136">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="cbd27-136">-CertificateFileContents</span></span>
<span data-ttu-id="cbd27-137">指定存取 Azure Data Lake Store 時將使用的憑證檔案內容。</span><span class="sxs-lookup"><span data-stu-id="cbd27-137">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="cbd27-138">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="cbd27-138">-CertificateFilePath</span></span>
<span data-ttu-id="cbd27-139">指定要用來驗證為服務主體之憑證的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="cbd27-139">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="cbd27-140">當存取 Azure Data Lake Store 時，該組會使用此功能。</span><span class="sxs-lookup"><span data-stu-id="cbd27-140">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="cbd27-141">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="cbd27-141">-CertificatePassword</span></span>
<span data-ttu-id="cbd27-142">指定要用來驗證為服務主體之憑證的密碼。</span><span class="sxs-lookup"><span data-stu-id="cbd27-142">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="cbd27-143">當存取 Azure Data Lake Store 時，該組會使用此功能。</span><span class="sxs-lookup"><span data-stu-id="cbd27-143">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="cbd27-144">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="cbd27-144">-ClusterName</span></span>
<span data-ttu-id="cbd27-145">指定組名。</span><span class="sxs-lookup"><span data-stu-id="cbd27-145">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="cbd27-146">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="cbd27-146">-ClusterSizeInNodes</span></span>
<span data-ttu-id="cbd27-147">指定該組群的工作者節點數目。</span><span class="sxs-lookup"><span data-stu-id="cbd27-147">Specifies the number of Worker nodes for the cluster.</span></span>

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

### <span data-ttu-id="cbd27-148">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="cbd27-148">-ClusterTier</span></span>
<span data-ttu-id="cbd27-149">指定 HDInsight 集區層級。</span><span class="sxs-lookup"><span data-stu-id="cbd27-149">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="cbd27-150">根據預設，這是標準。</span><span class="sxs-lookup"><span data-stu-id="cbd27-150">By default, this is Standard.</span></span>
<span data-ttu-id="cbd27-151">進一層只能與 Linux 系列一起使用，而且能使用一些新功能。</span><span class="sxs-lookup"><span data-stu-id="cbd27-151">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="cbd27-152">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="cbd27-152">-ClusterType</span></span>
<span data-ttu-id="cbd27-153">指定要建立之組群的類型。</span><span class="sxs-lookup"><span data-stu-id="cbd27-153">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="cbd27-154">選項為：Hadoop、HBase、Storm、Spark、INTERACTIVEHIVE、Kafka 和 RServer</span><span class="sxs-lookup"><span data-stu-id="cbd27-154">Options are: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka, and RServer</span></span>

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

### <span data-ttu-id="cbd27-155">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="cbd27-155">-ComponentVersion</span></span>
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

### <span data-ttu-id="cbd27-156">-ComputeIsolationHostSku</span><span class="sxs-lookup"><span data-stu-id="cbd27-156">-ComputeIsolationHostSku</span></span>
<span data-ttu-id="cbd27-157">為計算隔離獲取或設定專用主機 SKU。</span><span class="sxs-lookup"><span data-stu-id="cbd27-157">Gets or sets the dedicated host sku for compute isolation.</span></span>

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

### <span data-ttu-id="cbd27-158">-Config</span><span class="sxs-lookup"><span data-stu-id="cbd27-158">-Config</span></span>
<span data-ttu-id="cbd27-159">指定要用來建立該簇的組群物件。</span><span class="sxs-lookup"><span data-stu-id="cbd27-159">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="cbd27-160">此物件可以使用 Cmdlet New-AzHDInsightClusterConfig建立。</span><span class="sxs-lookup"><span data-stu-id="cbd27-160">This object can be created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="cbd27-161">-組式</span><span class="sxs-lookup"><span data-stu-id="cbd27-161">-Configurations</span></span>
<span data-ttu-id="cbd27-162">指定此 HDInsight 集區組。</span><span class="sxs-lookup"><span data-stu-id="cbd27-162">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="cbd27-163">您也可以使用 Add-AzHDInsightConfigValues Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cbd27-163">You can alternatively use the Add-AzHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="cbd27-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbd27-164">-DefaultProfile</span></span>
<span data-ttu-id="cbd27-165">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="cbd27-165">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cbd27-166">-部片公司Node</span><span class="sxs-lookup"><span data-stu-id="cbd27-166">-DisksPerWorkerNode</span></span>
<span data-ttu-id="cbd27-167">指定在組集中工作節點角色的磁片磁片數目。</span><span class="sxs-lookup"><span data-stu-id="cbd27-167">Specifies the number of disks for worker node role in the cluster.</span></span>

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

### <span data-ttu-id="cbd27-168">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="cbd27-168">-EdgeNodeSize</span></span>
<span data-ttu-id="cbd27-169">指定邊緣節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="cbd27-169">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="cbd27-170">針對Get-AzVMSize的 VM 大小使用資料，請參閱 HDInsight 的定價頁面。</span><span class="sxs-lookup"><span data-stu-id="cbd27-170">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="cbd27-171">此參數僅適用于 RServer 群。</span><span class="sxs-lookup"><span data-stu-id="cbd27-171">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="cbd27-172">-EnableComputeIsolation</span><span class="sxs-lookup"><span data-stu-id="cbd27-172">-EnableComputeIsolation</span></span>
<span data-ttu-id="cbd27-173">啟用 HDInsight 計算隔離功能。</span><span class="sxs-lookup"><span data-stu-id="cbd27-173">Enables HDInsight compute isolation feature.</span></span>

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

### <span data-ttu-id="cbd27-174">-EnableIDBroker</span><span class="sxs-lookup"><span data-stu-id="cbd27-174">-EnableIDBroker</span></span>
<span data-ttu-id="cbd27-175">啟用 HDInsight 身分識別識別識別識別功能。</span><span class="sxs-lookup"><span data-stu-id="cbd27-175">Enables HDInsight Identity Broker feature.</span></span>

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

### <span data-ttu-id="cbd27-176">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="cbd27-176">-EncryptionAlgorithm</span></span>
<span data-ttu-id="cbd27-177">獲取或設定加密演算法。</span><span class="sxs-lookup"><span data-stu-id="cbd27-177">Gets or sets the encryption algorithm.</span></span>

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

### <span data-ttu-id="cbd27-178">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="cbd27-178">-EncryptionAtHost</span></span>
<span data-ttu-id="cbd27-179">套用或設定旗標，指出是否要在主機啟用加密。</span><span class="sxs-lookup"><span data-stu-id="cbd27-179">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

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

### <span data-ttu-id="cbd27-180">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="cbd27-180">-EncryptionInTransit</span></span>
<span data-ttu-id="cbd27-181">套用或設定旗標，指出是否要在傳輸中啟用加密。</span><span class="sxs-lookup"><span data-stu-id="cbd27-181">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

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

### <span data-ttu-id="cbd27-182">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="cbd27-182">-EncryptionKeyName</span></span>
<span data-ttu-id="cbd27-183">獲取或設定加密金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="cbd27-183">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="cbd27-184">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="cbd27-184">-EncryptionKeyVersion</span></span>
<span data-ttu-id="cbd27-185">獲得或設定加密金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="cbd27-185">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="cbd27-186">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="cbd27-186">-EncryptionVaultUri</span></span>
<span data-ttu-id="cbd27-187">獲取或設定加密庫 uri。</span><span class="sxs-lookup"><span data-stu-id="cbd27-187">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="cbd27-188">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="cbd27-188">-HeadNodeSize</span></span>
<span data-ttu-id="cbd27-189">指定 Head 節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="cbd27-189">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="cbd27-190">針對Get-AzVMSize的 VM 大小使用資料，請參閱 HDInsight 的定價頁面。</span><span class="sxs-lookup"><span data-stu-id="cbd27-190">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="cbd27-191">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="cbd27-191">-HiveMetastore</span></span>
<span data-ttu-id="cbd27-192">指定 SQL 資料庫以儲存病毒中繼資料。</span><span class="sxs-lookup"><span data-stu-id="cbd27-192">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="cbd27-193">您也可以使用 Add-AzHDInsightMetastore Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cbd27-193">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="cbd27-194">-HTTPCredential</span><span class="sxs-lookup"><span data-stu-id="cbd27-194">-HttpCredential</span></span>
<span data-ttu-id="cbd27-195">指定該組 (HTTP) 組認證。</span><span class="sxs-lookup"><span data-stu-id="cbd27-195">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="cbd27-196">-KafkaClientGroupId</span><span class="sxs-lookup"><span data-stu-id="cbd27-196">-KafkaClientGroupId</span></span>
<span data-ttu-id="cbd27-197">取得或設定 Kafka Rest Proxy 存取的用戶端群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="cbd27-197">Gets or sets the client group id for Kafka Rest Proxy access.</span></span>

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

### <span data-ttu-id="cbd27-198">-KafkaClientGroupName</span><span class="sxs-lookup"><span data-stu-id="cbd27-198">-KafkaClientGroupName</span></span>
<span data-ttu-id="cbd27-199">取得或設定 Kafka Rest Proxy 存取的用戶端組名。</span><span class="sxs-lookup"><span data-stu-id="cbd27-199">Gets or sets the client group name for Kafka Rest Proxy access.</span></span>

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

### <span data-ttu-id="cbd27-200">-KafkaManagementNodeSize</span><span class="sxs-lookup"><span data-stu-id="cbd27-200">-KafkaManagementNodeSize</span></span>
<span data-ttu-id="cbd27-201">獲取或設定 Kafka 管理節點的大小。</span><span class="sxs-lookup"><span data-stu-id="cbd27-201">Gets or sets the size of the Kafka Management Node.</span></span>

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

### <span data-ttu-id="cbd27-202">-位置</span><span class="sxs-lookup"><span data-stu-id="cbd27-202">-Location</span></span>
<span data-ttu-id="cbd27-203">指定該組的位置。</span><span class="sxs-lookup"><span data-stu-id="cbd27-203">Specifies the location for the cluster.</span></span>

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

### <span data-ttu-id="cbd27-204">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="cbd27-204">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="cbd27-205">獲得或設定最小支援的 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="cbd27-205">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="cbd27-206">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="cbd27-206">-ObjectId</span></span>
<span data-ttu-id="cbd27-207">指定代表該 (之 Azure AD 服務) GUID 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="cbd27-207">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="cbd27-208">當存取 Azure Data Lake Store 時，該組會使用此功能。</span><span class="sxs-lookup"><span data-stu-id="cbd27-208">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="cbd27-209">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="cbd27-209">-OozieMetastore</span></span>
<span data-ttu-id="cbd27-210">指定儲存 Oozie 中繼資料的 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="cbd27-210">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="cbd27-211">您也可以使用 Add-AzHDInsightMetastore Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cbd27-211">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="cbd27-212">-OSType</span><span class="sxs-lookup"><span data-stu-id="cbd27-212">-OSType</span></span>
<span data-ttu-id="cbd27-213">指定該組群的作業系統。</span><span class="sxs-lookup"><span data-stu-id="cbd27-213">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="cbd27-214">選項有：Windows、Linux</span><span class="sxs-lookup"><span data-stu-id="cbd27-214">Options are: Windows, Linux</span></span>

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

### <span data-ttu-id="cbd27-215">-PrivateLink</span><span class="sxs-lookup"><span data-stu-id="cbd27-215">-PrivateLink</span></span>
<span data-ttu-id="cbd27-216">獲取或設定私人連結類型。</span><span class="sxs-lookup"><span data-stu-id="cbd27-216">Gets or sets the private link type.</span></span>

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

### <span data-ttu-id="cbd27-217">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="cbd27-217">-RdpAccessExpiry</span></span>
<span data-ttu-id="cbd27-218">指定遠端桌面通訊協定或 RDP (的 DateTime) 到期。</span><span class="sxs-lookup"><span data-stu-id="cbd27-218">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

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

### <span data-ttu-id="cbd27-219">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="cbd27-219">-RdpCredential</span></span>
<span data-ttu-id="cbd27-220">指定遠端桌面 (RDP) 組認證。</span><span class="sxs-lookup"><span data-stu-id="cbd27-220">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="cbd27-221">這僅適用于 Windows 系列。</span><span class="sxs-lookup"><span data-stu-id="cbd27-221">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="cbd27-222">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbd27-222">-ResourceGroupName</span></span>
<span data-ttu-id="cbd27-223">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cbd27-223">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="cbd27-224">-ResourceProviderConnection</span><span class="sxs-lookup"><span data-stu-id="cbd27-224">-ResourceProviderConnection</span></span>
<span data-ttu-id="cbd27-225">獲取或設定資源提供者連線類型。</span><span class="sxs-lookup"><span data-stu-id="cbd27-225">Gets or sets the resource provider connection type.</span></span>

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

### <span data-ttu-id="cbd27-226">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="cbd27-226">-ScriptActions</span></span>
<span data-ttu-id="cbd27-227">指定在建立組群結束時在組集中執行腳本動作。</span><span class="sxs-lookup"><span data-stu-id="cbd27-227">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="cbd27-228">您也可以使用 Add-AzHDInsightScriptAction。</span><span class="sxs-lookup"><span data-stu-id="cbd27-228">You can alternatively use Add-AzHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="cbd27-229">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="cbd27-229">-SecurityProfile</span></span>
<span data-ttu-id="cbd27-230">指定用來建立安全性群組組的安全性相關屬性。</span><span class="sxs-lookup"><span data-stu-id="cbd27-230">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="cbd27-231">您也可以使用 Add-AzHDInsightSecurityProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cbd27-231">You can alternatively use the Add-AzHDInsightSecurityProfile cmdlet.</span></span>

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

### <span data-ttu-id="cbd27-232">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="cbd27-232">-SshCredential</span></span>
<span data-ttu-id="cbd27-233">指定要用於 SSH 連接的 SSH 認證。</span><span class="sxs-lookup"><span data-stu-id="cbd27-233">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="cbd27-234">這僅適用于 Linux 系列。</span><span class="sxs-lookup"><span data-stu-id="cbd27-234">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="cbd27-235">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="cbd27-235">-SshPublicKey</span></span>
<span data-ttu-id="cbd27-236">指定要用於 SSH 連接的公用鍵。</span><span class="sxs-lookup"><span data-stu-id="cbd27-236">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="cbd27-237">這僅適用于 Linux 系列。</span><span class="sxs-lookup"><span data-stu-id="cbd27-237">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="cbd27-238">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="cbd27-238">-StorageAccountKey</span></span>
<span data-ttu-id="cbd27-239">取得或設定儲存空間帳戶的儲存空間帳戶訪問金鑰。</span><span class="sxs-lookup"><span data-stu-id="cbd27-239">Gets or sets the Storage Account Access Key for the Storage Account.</span></span>

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

### <span data-ttu-id="cbd27-240">-StorageAccountManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="cbd27-240">-StorageAccountManagedIdentity</span></span>
<span data-ttu-id="cbd27-241">獲取或設定儲存空間帳戶受管理的身分識別。</span><span class="sxs-lookup"><span data-stu-id="cbd27-241">Gets or sets the storage account managed identity.</span></span>

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

### <span data-ttu-id="cbd27-242">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="cbd27-242">-StorageAccountResourceId</span></span>
<span data-ttu-id="cbd27-243">為儲存空間帳戶獲取或設定儲存資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="cbd27-243">Gets or sets the Storage Resource Id for the Storage Account.</span></span>

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

### <span data-ttu-id="cbd27-244">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="cbd27-244">-StorageAccountType</span></span>
<span data-ttu-id="cbd27-245">獲取或設定儲存空間帳戶的類型。</span><span class="sxs-lookup"><span data-stu-id="cbd27-245">Gets or sets the type of the storage account.</span></span>

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

### <span data-ttu-id="cbd27-246">-StorageContainer</span><span class="sxs-lookup"><span data-stu-id="cbd27-246">-StorageContainer</span></span>
<span data-ttu-id="cbd27-247">為預設的 Azure 儲存空間帳戶獲取或設定 StorageContainer 名稱</span><span class="sxs-lookup"><span data-stu-id="cbd27-247">Gets or sets the StorageContainer name for the default Azure Storage Account</span></span>

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

### <span data-ttu-id="cbd27-248">-StorageFileSystem</span><span class="sxs-lookup"><span data-stu-id="cbd27-248">-StorageFileSystem</span></span>
<span data-ttu-id="cbd27-249">為預設的 Azure Data Lake Storage Gen2 帳戶獲取或設定檔案系統。</span><span class="sxs-lookup"><span data-stu-id="cbd27-249">Gets or sets the file system for the default Azure Data Lake Storage Gen2 account.</span></span>

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

### <span data-ttu-id="cbd27-250">-StorageRootPath</span><span class="sxs-lookup"><span data-stu-id="cbd27-250">-StorageRootPath</span></span>
<span data-ttu-id="cbd27-251">在預設的 Data Lake 市集帳戶中，獲取或設定該組根目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="cbd27-251">Gets or sets the path to the root of the cluster in the default Data Lake Store Account.</span></span>

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

### <span data-ttu-id="cbd27-252">-子網名稱</span><span class="sxs-lookup"><span data-stu-id="cbd27-252">-SubnetName</span></span>
<span data-ttu-id="cbd27-253">為此 HDInsight 組組獲取或設定子網名稱。</span><span class="sxs-lookup"><span data-stu-id="cbd27-253">Gets or sets the subnet name for this HDInsight cluster.</span></span>

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

### <span data-ttu-id="cbd27-254">-版本</span><span class="sxs-lookup"><span data-stu-id="cbd27-254">-Version</span></span>
<span data-ttu-id="cbd27-255">指定 HDInsight 集區 HDI 版本。</span><span class="sxs-lookup"><span data-stu-id="cbd27-255">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="cbd27-256">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="cbd27-256">-VirtualNetworkId</span></span>
<span data-ttu-id="cbd27-257">指定要配置該組集的虛擬網路的識別碼。</span><span class="sxs-lookup"><span data-stu-id="cbd27-257">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="cbd27-258">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="cbd27-258">-WorkerNodeSize</span></span>
<span data-ttu-id="cbd27-259">指定工作節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="cbd27-259">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="cbd27-260">針對Get-AzVMSize的 VM 大小使用資料，請參閱 HDInsight 的定價頁面。</span><span class="sxs-lookup"><span data-stu-id="cbd27-260">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="cbd27-261">-KeeperkeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="cbd27-261">-ZookeeperNodeSize</span></span>
<span data-ttu-id="cbd27-262">指定資料管理節點的虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="cbd27-262">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="cbd27-263">針對Get-AzVMSize的 VM 大小使用資料，請參閱 HDInsight 的定價頁面。</span><span class="sxs-lookup"><span data-stu-id="cbd27-263">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="cbd27-264">此參數僅適用于 HBase 或暴風雪組。</span><span class="sxs-lookup"><span data-stu-id="cbd27-264">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="cbd27-265">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbd27-265">CommonParameters</span></span>
<span data-ttu-id="cbd27-266">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cbd27-266">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbd27-267">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cbd27-267">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbd27-268">輸入</span><span class="sxs-lookup"><span data-stu-id="cbd27-268">INPUTS</span></span>

### <span data-ttu-id="cbd27-269">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="cbd27-269">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="cbd27-270">輸出</span><span class="sxs-lookup"><span data-stu-id="cbd27-270">OUTPUTS</span></span>

### <span data-ttu-id="cbd27-271">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="cbd27-271">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="cbd27-272">筆記</span><span class="sxs-lookup"><span data-stu-id="cbd27-272">NOTES</span></span>
<span data-ttu-id="cbd27-273">關鍵字：azure、azurerm、arm、resource、management、manager、hadoop、hdinsight、hd、insight</span><span class="sxs-lookup"><span data-stu-id="cbd27-273">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="cbd27-274">相關連結</span><span class="sxs-lookup"><span data-stu-id="cbd27-274">RELATED LINKS</span></span>

[<span data-ttu-id="cbd27-275">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="cbd27-275">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

